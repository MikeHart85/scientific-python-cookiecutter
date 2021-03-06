===========================
Philosophy of this Tutorial
===========================

We aim to nudge scientist--developers toward good practices and standard tools,
to help small- and medium-sized projects start off on the right foot. Keeping
in mind that too much development infrastructure can be overwhelming to those
who haven't yet encountered the need for it, we stop short of recommending the
*full* stack of tools used by large scientific Python projects.

This is an opinionated tutorial. We guide readers toward certain tools and
conventions. We do not always mention alternatives and their respective
trade-offs because we want to avoid overwhelming beginners with too many
decisions. Our choices are based on the current consensus in the scientific
Python community and the personal experience of the authors.

The Tools, and the Problems They Solve
--------------------------------------

..
   Note: The bolded items here are intentionally not links. These things are
   easy enough to Google if people want to know more, and I'd like to avoid
   scaring anyone off by making them feel like they need to review the project
   home pages for each of these projects before proceeding.

* **Python 3** has been around since 2008, and it gained real traction in the
  scientific Python ecosystem around 2014. It offers
  `many benefits for scientific applications <https://python-3-for-scientists.readthedocs.io/en/latest/>`_.
  Python 2 will reach its end-of-life (no new security updates) in 2020. Some
  projects still support both 2 and 3, but many have already dropped support
  for Python 2 in new releases or
  `publicly stated their plans to do so <https://python3statement.org/>`_.
  This cookiecutter focuses on Python 3 only.
* **Pip** is the official Python package manager, and it can install packages
  either from code on your local machine or by downloading them from the Python
  Package Index (PyPI).
* **Git** is a version control system that has become the consensus choice. It
  is used by virtually all of the major scientific Python projects, including
  Python itself.
* **GitHub** is a website, owned by Microsoft, for hosting git repositories and
  discussion between contributors and users.
* **Cookiecutter** is a tool for generating a directory of files from a
  template. We will use it to generate the boilerplate scaffolding of a Python
  project and various configuration files without necessarily understanding all
  the details up front.
* **PyTest** is a framework for writing code that tests other Python code.
  There are several such frameworks, but pytest has emerged as the favorite,
  and major projects like numpy have switched from older systems to pytest.
* **Flake8** is a tool for inspecting code for likely mistakes (such as a
  variable that is defined but never used) and/or inconsitent style. This tool
  is right "on the line" as far as what we would recommend for beginners. Your
  mileage may vary, and so the tutorial includes clear instructions for
  ommitting this piece.
* **Travis-CI** is an online service, free for open-source projects, that
  speeds software development by checking out your code on a fresh, clean
  server, installing your software, running the tests, and reporting the
  results. This helps you ensure that your code will work on your colleague’s
  computer---that it doesn’t accidentally depend on some local detail of your
  machine.  It also creates a clear, public record of whether the tests passed
  or failed, so if things are accidentally broken (say, while you are on
  vacation) you can trace when the breaking change occurred.
* **RestructuredText** (``.rst``) is a markup language, like HTML. It is
  designed for writing software documentation. It is used by almost all
  scientific Python projects, large and small.
* **Sphinx** is a documentation-publishing tool that renders
  RestructuredText into HTML, PDF, LaTeX, and other useful formats. It also
  inspects Python code to extract information (e.g. the list of functions in a
  module and the arguments they expect) from which it can automatically
  generate documentation. Extensions for sphinx provide additional
  functionality, some of which we cover in this tutorial.
* **GitHub Pages** is a free service for publishing static websites. It is
  suitable for publishing the documentation generated by sphinx.
