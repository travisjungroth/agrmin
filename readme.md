# Agrmin: Simple Websites

Agrmin (short for Agressive Minimalism) is a script for generating a simple one page website from MultiMarkdown files. It was written to generate a website of short stories and articles. The CSS was taken from [bettermotherfuckingwebsite.com](http://bettermotherfuckingwebsite.com/) and slightly modified.

### Setup
To build a site with agrmin, the easiest thing is to clone from GitHub and delete the local repo.

    git clone https://github.com/travisjungroth/agrmin.git project_name
    cd project_name
    rm -rf .git
    
You can then start a new repo with `git init`, make your first commit and [push your code to GitHub](https://help.github.com/articles/adding-an-existing-project-to-github-using-the-command-line/).

### Usage
The code includes a sample site and is easiest to just modify as needed. To generate the web page, `main.py`. This creates `index.html`.

    python3 main.py

`static/header.html` and `static/footer.html` are static files that get added to the top and bottom of `index.html`. Modify them directly.

Posts are content such as articles and stories saved as MultiMarkdown files. The links at the top of the page and the headers for each post are generated from the Title meta attribute in the file.

Posts are added by creating a MultiMarkdown file in `posts` and adding the file name to the `post_paths` tuple in `main.py`. They appear in the same order on the web page as they do in the tuple.

### FAQ

##### Why don't you support Date/Author/Other Meta Attribute
 Because I didn't need it. Go nuts on `main.py` to add whatever you need.
 
##### What if I want more than one web page?
You should definitely use something else. Check out [Pelican](http://blog.getpelican.com/) and [MkDocs](http://www.mkdocs.org/)

##### Why are my HTML changes disappearing?
Make sure you're editing the static files and not `index.html`.

##### How's the test coverage?
Haha no.

##### I have an index.html file. Now what?
Now you need to host it. Amazon S3 makes this super cheap and easy.

