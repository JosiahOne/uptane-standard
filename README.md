# Uptane IEEE-ISTO Standard

[Uptane](https://uptane.github.io) is the first compromise-resilient software update security system for the automotive industry. Beginning in 2018, a working group has begun the process of describing the system's design, implementation, and deployment considerations as a formal standard, working as an [IEEE-ISTO](https://ieee-isto.org/) industry group. This repository is the public home of that standardization work.

## Existing documentation

Several documents are already available which describe Uptane's design and implementation. Note that an intial version of the Uptane Standards document has been developed and should be considered the authoritative resource for the framework:

* [Uptane Standards Document](https://uptane.github.io/uptane-standard/uptane-standard.html)
* [Reference Implementation and Demonstration Code](https://github.com/uptane/uptane)

## Contributing

The standard is being written in [RFC 2629](https://tools.ietf.org/html/rfc2629)/[RFC 7749](https://tools.ietf.org/html/rfc7749) format, using markdown as a source. Comments, issues, and pull requests are welcome.

We use [GitHub Flow](https://guides.github.com/introduction/flow/) for contributing content. When you are working on a section, make a branch off the current master, and submit a pull request when it's ready to merge. If github reports any merge conflicts in the PR, please rebase until the merge can be done cleanly.

### Commit messages and squashes

Use clear, informative commit messages, and squash any minor commits that do not represent an actual contribution of content (e.g. typo fixes). It is not necessary to squash all your commits when submitting a PR, but please try to keep the commit history reasonably clean.

### Text formatting

Don't use fixed-width columns. The `plaintext` rendering target will produce a text file with fixed-width columns; using fixed-width columns in the markdown source just makes the diffs harder to read.

## Building/rendering the document

We use [kramdown-rfc2629](https://github.com/cabo/kramdown-rfc2629) to render the markdown source into xml, and [xml2rfc](https://xml2rfc.tools.ietf.org/) to render the XML into HTML or plaintext. A Makefile is included for convenience. You can also render using [Docker](https://www.docker.com/) if you don't wish to install the tools. See `make help` for options.

### Pushing to github pages

The rendered HTML from the markdown source at `master` will be available at https://uptane.github.io/uptane-standard/uptane-standard.html. You can update this, if you have commit rights to this repository, by pushing `uptane-standard.html` to the `gh-pages` branch.

TODO: Set up CI to auto-push on merge to master.
