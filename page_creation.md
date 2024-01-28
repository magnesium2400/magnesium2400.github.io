---
layout: default
title: Page Creation
---

# Creating a Simple GitHub Pages Site (2024-01)

## 0. Create a `.io` project
- If you want to create a webpage for a particular repo, this step is not required.
- If you want to create a general homepage, create a project called `<<my_github_username>>.github.io`.

## 1. Set up GitHub pages on the repo you want
1. Under the repo go to **Settings** in the toolbar on the top.
2. Go the **Pages** section on the toolbar on the left.
3. Under *Build and deployment*: set *Source* to 'Deploy from a branch' and set *Branch* to the chosen branch. You can also set a folder to deploy from (e.g. `./docs`) if the docs will not be contained in the root folder. 

## 2. Create `_config.yml`
1. In the folder that was selected as the folder to deploy from, create a file called `_config.yml`.
2. Add in this line: `remote_theme: just-the-docs/just-the-docs`, as well as any other data you want to add (see the [just-the-docs] documentation for more details).

## 3. Add your pages as `.md` files
- You can add information in YAML frontmatter e.g. `layout`, `name`, or `permalink`. 


[just-the-docs]: https://just-the-docs.com/








