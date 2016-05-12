# Starterkit

The source code for the website for the [LHCb Starterkit][the-site] organisation.

## Building the website

The site is [built automatically][gh-pages] whenever the [`gh-pages` 
branch][gh-pages-branch] is updated on GitHub.

To build the site locally, you need to install the [`github-pages` 
gem][gh-pages-gem] and then run [Jekyll][jekyll], a program that converts the 
collection of HTML templates and [Markdown][md] files in this repository to 
full HTML pages. Assuming you have [Ruby][ruby] installed on your machine, 
which should be the case on anything but Windows, inside this repository you 
can do:

```bash
$ gem install bundler
$ bundle install --path=vendor/bundle
$ bundle exec jekyll build
```

(The use of the `--path` option in `bundle install` and of `bundle exec` makes 
the dependency installation local to the folder containing the repository, so 
that your ‘global’ list of gems isn't touched.)

This will build the site into the `_site` directory, and you can then open 
`_site/index.html` in your browser to see the site.

To have Jekyll monitor the repository for changes and serve the website on a 
local development server, do:

```bash
$ bundle exec jekyll serve --watch
```

You can visit the site using the local address 
[`http://127.0.0.1:4000/starterkit/`][local-addr].

[the-site]: https://lhcb.github.io/starterkit
[gh-pages]: https://pages.github.com/
[gh-pages-branch]: https://github.com/lhcb/starterkit/tree/gh-pages
[gh-pages-gem]: https://github.com/github/pages-gem
[jekyll]: https://jekyllrb.com/
[md]: https://guides.github.com/features/mastering-markdown/
[ruby]: https://www.ruby-lang.org/
[local-addr]: http://127.0.0.1:4000/starterkit/
