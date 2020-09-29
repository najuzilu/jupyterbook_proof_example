# Utilizing Jupyter Book with sphinxcontrib-prettyproof

Below are some instructions on how to setup a Jupyter Book example and utilize the sphinxcontrib-prettyproof extension.

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
