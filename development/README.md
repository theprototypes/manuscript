<br>

The repository's development notes.

<br>
<br>

## Remote Development

The development image depends on

* [requirements.txt](/.devcontainer/requirements.txt)
* [Dockerfile](/.devcontainer/Dockerfile)

The requirements file lists the packages/libraries required for development.  The image is built via the command

```shell
docker build . --file .devcontainer/Dockerfile --tag design
```

Subsequently, a development container is initialised via the command

```shell
docker run --rm -i -t -p 127.0.0.1:10000:8050 -w /app --mount type=bind,src="$(pwd)",target=/app design
```

<br>

Herein, `-p 10000:8050` maps the host port `10000` to container port `8050`.  Note, the container's working environment, i.e., -w, must be inline with this project's top directory.  In brief:

* --rm: [automatically remove container](https://docs.docker.com/engine/reference/commandline/run/#:~:text=a%20container%20exits-,%2D%2Drm,-Automatically%20remove%20the)
* -i: [interact](https://docs.docker.com/engine/reference/commandline/run/#:~:text=and%20reaps%20processes-,%2D%2Dinteractive,-%2C%20%2Di)
* -t: [tag](https://docs.docker.com/get-started/02_our_app/#:~:text=Finally%2C%20the-,%2Dt,-flag%20tags%20your)
* -p: [publish a container's ports to its host](https://docs.docker.com/engine/reference/commandline/run/#:~:text=%2D%2Dpublish%20%2C-,%2Dp,-Publish%20a%20container%E2%80%99s)


<br>
<br>

## Sphinx

Initialise Sphinx via

```shell
mkdir docs && cd docs && sphinx-quickstart
cd ..
```

Build pages via

```shell
sphinx-build -E -b html docs/source docs/build/html
```

Logo

```markdown
.. image:: _static/logo.svg
```

<br>

### References

**SPHINX**

* [Sphinx](https://www.sphinx-doc.org/en/master/index.html)
  * [Sphinx Directives](https://www.sphinx-doc.org/en/master/usage/restructuredtext/directives.html)
* [reStructuredText](https://docutils.sourceforge.io/rst.html)
  * [Sphinx reStructuredText Primer](https://www.sphinx-doc.org/en/master/usage/restructuredtext/index.html)
  * [reStructuredText Card](https://bashtage.github.io/sphinx-material/rst-cheatsheet/rst-cheatsheet.html)
* [MyST](https://myst-parser.readthedocs.io/en/latest/index.html)
  * [Organising Content](https://myst-parser.readthedocs.io/en/latest/syntax/organising_content.html#using-toctree-to-include-other-documents-as-children)
  * [configuration](https://myst-parser.readthedocs.io/en/latest/configuration.html)
  * [cross-referencing](https://myst-parser.readthedocs.io/en/latest/syntax/cross-referencing.html#)
* [Extensions](https://myst-parser.readthedocs.io/en/latest/intro.html#extending-sphinx)
  * [mermaid](https://mermaid.js.org/intro/)
  * [tippy](https://sphinx-tippy.readthedocs.io/en/latest/)
  * [issues](https://github.com/sloria/sphinx-issues)
* Font
  * [inter](https://fonts.google.com/selection?query=inter)
  * [vollkorn](https://fonts.google.com/specimen/Vollkorn)
  * [embedding](https://fonts.google.com/selection/embed)
* Badges
  * [shields](https://shields.io)
  * [static shields badges](https://shields.io/badges/static-badge)
  * [static shield badge example](https://img.shields.io/badge/issue-6511-green)
  * [Shields Tutorial](https://github.com/badges/shields/blob/master/doc/TUTORIAL.md)


<br>


**SPHINX BOOK THEME**

* [Sphinx Book Theme](https://sphinx-book-theme.readthedocs.io/en/stable/index.html)
  * [Sample](https://sphinx-book-theme.readthedocs.io/en/stable/reference/kitchen-sink/index.html)
* [Sphinx Design: Sphinx Book Theme](https://sphinx-design.readthedocs.io/en/sbt-theme/)
* Configuration
  * [Theme Options](https://sphinx-book-theme.readthedocs.io/en/stable/reference.html#reference-of-theme-options)
  * [Theme Options: Basic](https://pydata-sphinx-theme.readthedocs.io/en/latest/user_guide/layout.html#references)
  * [Sidebar: Secondary](https://sphinx-book-theme.readthedocs.io/en/stable/sections/sidebar-secondary.html)


<br>


**MEASURES**

* [`em` & `px`](https://nekocalc.com/em-to-px-converter)


<br>


**HTML (HyperText Markup Language)**

* Tabs: [1](https://www.html-easy.com/learn/how-to-add-tabs-in-html/), [2](https://www.w3schools.com/howto/howto_js_tabs.asp), [3](https://squidfunk.github.io/mkdocs-material/reference/content-tabs/)

<br>
<br>

<br>
<br>

<br>
<br>

<br>
<br>
