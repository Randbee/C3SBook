# C3SBook

This repository contains a book of notebooks generated with Jupyter Book. Below are the instructions for working with this project, including how the structure of the notebooks works and how to perform the build and deploy process of the book.

## Notebook and Submodule Structure

The book of notebooks is organized using submodules, which allows for maintaining a modular structure and facilitates managing the different topics and sections of the book. Each submodule is a training book and it's uploaded in GitHub as a repository. The submodule structure is defined in the `_toc.yml` file and stored in `notebooks` directory.

## Building and Deploying the Book

To build and deploy the book of notebooks, follow these steps:

### 1. Create a Development Environment

Before building the book, ensure you have a development environment with all the necessary dependencies installed. You can create a virtual environment with the dependencies using the following command:

```bash
. ./developer/create-environment-for-build
```

### 2. Rebuild the Book

To rebuild the book, first remove the existing `_build` folder and then run the following command to rebuild the book:

```bash
rm -rf _build
jupyter-book build --all .
```

### 3. Book Deployment

Once the book has been successfully rebuilt, you can deploy it to the `gh-pages` branch using `ghp-import`. Run the following command to copy the `_build/html` folder to the `gh-pages` branch and deploy the book:

```bash
ghp-import -n -p -f _build/html
```