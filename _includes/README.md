# Carto UI Developer Test

This project contains an implementation of the [UI developer job application test](https://gist.github.com/jimartincorral/72c04dd47424713cc40d254af55ff69f). For the implementation, I have used Jekyll and Contentful as Headless CMS to fetch images, text and videos for the page.

## Instalation

### 1. Prerequisites

First of all, we will need to install Jekyll. For a step to step explanation on how to install it in your machine follow the Jekyll docs --> https://jekyllrb.com/docs/.

### 2. Run the development server

On the project root folder, run the following comands:

```bash
echo "Install Dependencies"        && bundle install && \
echo "Fetch Contentful Data"       && bundle exec jekyll contentful && \
echo "Start Jekyll Server"         && bundle exec jekyll server
```

After that, you can open a browser and go to [localhost:4000](http://localhost:4000).
If you want to reproduce the youtube videos, you must go to the localhost URL instead of the loopback IP (127.0.0.1).

### 3. Build static page

To build the page, you should have run `bundle install` and `bundle exec jekyll contentful` before.

For building the static site, run:

```bash
 jekyll build
```

After that, you will find the static site in the folder `/_site`

## Some possible improvements

It would have been nice to declare variables for the font sizes, font weights, line heights, letter spacings and elements separations to reuse common styles across the page.
