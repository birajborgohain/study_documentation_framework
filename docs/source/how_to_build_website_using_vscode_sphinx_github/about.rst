Getting Started with Sphinx
===========================

Introduction
------------

Sphinx is a powerful documentation generator that converts files written in
**reStructuredText (``.rst``)** into a professional HTML website. It is widely
used for software documentation, research projects, technical manuals, books,
and educational websites.

Prerequisites
-------------

Before creating your first documentation website, install the following software:

* Python 3
* Visual Studio Code (VS Code)
* Sphinx

Creating a New Sphinx Project
-----------------------------

Open **Visual Studio Code** and launch the integrated terminal.

Navigate to the directory where you want to create your project and run:

.. code-block:: bash

   sphinx-quickstart

Follow the prompts to configure your project. Sphinx will automatically create
the necessary files and directories.

Project Structure
-----------------

A typical Sphinx project has the following structure:

.. code-block:: text

   project/
   ├── Makefile
   ├── make.bat
   ├── source/
   │   ├── conf.py
   │   ├── index.rst
   │   └── ...
   └── build/

Writing Documentation
---------------------

Write your documentation inside the ``source`` directory. The homepage of the
website is usually ``index.rst``. Additional pages can be created as separate
``.rst`` files and linked together using the ``toctree`` directive.

Building the Website
--------------------

Open a terminal in the project directory (where the ``Makefile`` is located)
and build the website by running:

.. code-block:: bash

   make html

Sphinx converts the source files into HTML and stores the generated website in
the ``build/html`` directory.

Viewing the Website
-------------------

To open the generated website, open the following file in your web browser:

.. code-block:: text

   build/html/index.html

Alternatively, start a local web server by running:

.. code-block:: bash

   python -m http.server 8000 --directory build/html

Then open your web browser and visit:

.. code-block:: text

   http://127.0.0.1:8000

Development Workflow
--------------------

The typical workflow for developing documentation is:

1. Open the project in VS Code.
2. Edit the ``.rst`` files.
3. Save your changes.
4. Run:

   .. code-block:: bash

      make html

5. Refresh the browser to preview the latest version of the website.

Publishing the Website
----------------------

After completing the documentation, you can publish it online by:

* Initializing a Git repository.
* Pushing the project to GitHub.
* Connecting the GitHub repository to Read the Docs.
* Allowing Read the Docs to automatically build and publish the website whenever changes are pushed to GitHub.

Summary
-------

Using **VS Code**, **Sphinx**, **Git**, **GitHub**, and **Read the Docs**
provides a modern and professional workflow for creating, maintaining, and
publishing documentation websites. This workflow is widely adopted by software
developers, researchers, educators, and open-source communities because it
supports version control, collaboration, and automatic website deployment.