Welcome to your Jupyter Book
============================

This is a small sample book to give you a feel for how book content is
structured.

Check out the content pages bundled with this sample book to get started.

## Steps taken to create this book

```bash
conda create -n myproofbook pip
conda activate myproofbook
pip install jupyter-book
pip install sphinxcontrib-prettyproof

jupyter-book create myproofbook
cd myproofbook
```

Add extension under `_config.yml`:

```yaml
sphinx:
  extra_extensions:
    - sphinxcontrib.prettyproof
```

Now introduce proof and theorem directives:

```{proof:proof}
This is a proof directive.
```

```{proof:theorem} Title of theorem
This is a theorem directive.
```

Next build the book:

```bash
jb clean .
jb build .
```
