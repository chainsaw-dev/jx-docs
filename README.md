# Jenkins X Docs

Documentation site for [Jenkins X](http://jenkins-x.io/)

**Please browse these docs** on the [http://jenkins-x.io/](http://jenkins-x.io/) site as the links don't all work when browsing the markdown files inside github


## Build the docs locally

To edit the docs locally and try out what the [website](http://jenkins-x.io/) will look like then you need to clone this repository:

```bash
$ git clone https://github.com/jenkins-x/jx-docs.git
```

### Dockerized Hugo

Instead of installing Hugo locally, you can use the included `docker-compose.yml` to spin up the Hugo server. Make sure you have Docker installed.

* Build and run the preview server: `docker-compose up -d server`
* go to http://localhost:1313 to view the site

### Local Hugo install

Then to view the docs in your browser, [install Hugo](https://gohugo.io/getting-started/installing).
Navigate to the directory, run hugo server, and open up the link:

```bash
$ cd jx-docs
$ hugo server

Started building sites ...
.
.
Serving pages from memory
Web Server is available at http://localhost:1313/ (bind address 127.0.0.1)
Press Ctrl+C to stop
```
### Running spell check

We're not all masters of spelling, so luckily there's tools to help us fix that. We'll be using [node-markdown-spellcheck](https://github.com/lukeapage/node-markdown-spellcheck) to run through all our markdown files and list any spelling issue or unknown word it can find.

To make this as simple as possible, just run the following command

```bash
$ docker-compose up spellchecker
```

This will output any issue the spell checker have found.

It's likely that the report includes words that are spelled correctly, but that just means the spell checker is not aware of the correct spelling (happens a lot for technical terms, commands, etc.). Please edit the `.spelling` file and add the unknown word.
Also, please try and keep the list alphabetically sorted; makes it easier to navigate when you're looking for something

# Contribution

Please visit the contributing guide for the documentation available at [Jenkins X website](https://jenkins-x.io/contribute/documentation/).

## Localization

In order to let more people know Jenkins X better, localization is very important and meaningful. And we should keep some rules about this, please read related languages below:

* [Chinese](Localization_Chinese.md)
