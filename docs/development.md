# Developing the site

The site consists of two components:

+ The theme, [`leeds_pgr_basic`](https://github.com/leeds-maths-pgr/leeds_pgr_basic), which is a submodule of
+ the main site project, [`conf-2023`](https://github.com/leeds-maths-pgr/conf-2023).

Broadly speaking, `leeds_pgr_basic` contains the general CSS and templating code, while `conf-2023` contains the site content and specific additions e.g. the schedule and speaker templating code.
When developing the site, you will have to work on these two projects simultaneously.

## Getting started

+ [Installing Hugo](#installing-hugo)
+ [Pull requests](#pull-requests)


## Installing Hugo

The site is generated with the [Hugo](https://gohugo.io/) static site generator and uses [SCSS](https://sass-lang.com/) to generate the stylesheets.
Both are packaged into a single binary available [here](https://gohugo.io/installation/).

The benefit of using an SSG as opposed to writing the HTML by hand is that there is a good separation between content and markup.
Content authors do not need to worry about markup, and designers do not need to be on hand to help with writing content.
The templates also enforce a particular semantic structure on the content, which can minimise the complexity of the stylesheet.

We use SCSS as opposed to CSS as the former has many useful features that aren't present in CSS (e.g. mixins and loops).
Moreover, valid CSS is valid SCSS, and we compile the SCSS to CSS during deployment, so there is no loss of expressiveness.

Once Hugo is installed and visible on your PATH, test it by:
+ cloning the repository with `git clone --recursive git@github.com:leeds-maths-pgr/conf-2023.git`,
+ changing directory, `cd conf-2023`,
+ running the local Hugo test server, `hugo serve`

Among the information printed will be a link saying where the website is served, it should be of the form `http://localhost:<PORT>/conf-2023/`.
Open this in a web browser and verify that the site is being served locally by making a test change in the content directory.

## Pull Requests
