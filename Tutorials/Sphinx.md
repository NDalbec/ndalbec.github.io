# Document creation using Sphinx

Install

```
pip install Sphinx
```

Make html from files 

```
make html
```
Or
```
.\make html
```


# Host on GitHub

https://github.com/sphinx-doc/sphinx/issues/3382

1. Create a folder `docs` in the root path.

2. By default, Jekyll does not build any files or directories with underscore. Include an empty `.nojekyll` file in the docs folder to turn off Jekyll.

3. In the docs folder, create an `index.html` file and redirect to `./html/index.html` for example like this:

```
<meta http-equiv="refresh" content="0; url=./html/index.html" />
```

4. Change the Sphinx build directory to `docs` in your `Makefile` and `make.bat` (to modify `make.bat` go to more options and select edit) for example as follows:

```
BUILDDIR      = docs
```

5. Run `make html` then add, commit and push the repo.

6. In your project config, choose to use the docs folder for your GitHub Pages.

7. The page is available at https://<username>.github.io/<repo>
