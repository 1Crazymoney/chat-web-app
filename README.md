# gatsby-ipfs-boilerplate

This repository (*repo*) contains a website template for building a website with
the [Gatsby framework](https://www.gatsbyjs.org/).

- [Live Demo](http://troutsblog.com)
- [Mirror](https://ipfs.io/ipfs/QmbG75ohG6oKrnDFiWXVAtTc79pfyELNjZ9cvhYRMyyN2q/)

Unlike other Gatsby starters and website templates, this template has some
specific features:
- Markdown support added. Easily create new research articles and blog posts.
Save your markdown files to the [markdown](./markdown) directory.
- [IPFS](https://ipfs.io) ready. The `public` folder where the site gets built
is ready to be added to the IPFS network, and will serve the website from any
IPFS gateway. [Here's an example](https://ipfs.io/ipfs/QmbG75ohG6oKrnDFiWXVAtTc79pfyELNjZ9cvhYRMyyN2q/)
- Responsive and Mobile First. The site template is originally based
on [Fourty by HTML5 Up](https://github.com/codebushi/gatsby-starter-forty). It
features mobile-first styling and easy-to-use grid system for controlling the
mobile and desktop displays.

This template is intended to work in concert with two other pieces of software:
- The [koa-ipfs-blog](https://github.com/christroutner/koa-ipfs-blog) is the back-end
server intended to serve up the website generated by this front end repository.
It serves the content in a conventional way, but also syndicates it over the
IPFS and Tor networks.
- The [memo-push](https://github.com/christroutner/memo-push) tool is used to
publish the IPFS link on the Bitcoin Cash blockchain, using
the [Memo.cash](https://memo.cash) protocol.

Together, these three pieces of software can publish progressive web apps in a
way that is very hard to censor. They were created to encourage developers to
combine the forces of Bitcoin Cash, IPFS, and Tor to unleash a vibrant online
economy.

- [Here is a non-technical video](https://www.youtube.com/watch?v=RlNVyatwd5M) overview
of how governments censor content on the internet, and how decentralized publishing
tools can be used to circumvent it.

- [Here is a walkthrough video](https://www.youtube.com/watch?v=Ez9YXpu_Chs&t=971s) of
how to use this repository along with
the [memo-push](https://github.com/christroutner/memo-push) tool to publish a
website in a decentralized, censorship-resistant way in order to leverage the
[Streisand Effect](https://en.wikipedia.org/wiki/Streisand_effect).

## Installation

Install this starter
(assuming [Gatsby is installed](https://www.gatsbyjs.org/docs/gatsby-cli/)) by
running from your CLI:
<br/>
`gatsby new gatsby-ipfs-boilerplate https://github.com/christroutner/gatsby-ipfs-boilerplate`

Run `gatsby develop` in the terminal to start the dev site.

## CSS Grid

The grid on this site was replaced with a custom version, built using CSS Grid. It's a very simple 12 column grid that is disabled on mobile. To start using the grid, wrap the desired items with `grid-wrapper`. Items inside the `grid-wrapper` use the class `col-` followed by a number, which should add up to 12.

Here is an example of using the grid, for a 3 column layout:

```
<div className="grid-wrapper">
    <div className="col-4">
        <p>Content Here</p>
    </div>
    <div className="col-4">
        <p>Content Here</p>
    </div>
    <div className="col-4">
        <p>Content Here</p>
    </div>
</div>
```

## Markdown

By default, the website offers two different areas to post your markdown files
inside the [markdown](./markdown) directory:
- The `blog` directory will add your file to the `/blog` page, sorted by date.
- The `research` directory will list articles based on topics, on the
`/research` page. These articles are ordered by topic instead of by date.
Topics correspond to the subdirectories in the `research` directory.

## IPFS
v1.0.1 uploaded to IPFS with npm dependencies:
- Get repository: `ipfs get QmSvmWaRFZp9psEfA5BaVpVR7MKJUtwdoWnN2Qq6PKXTXL`
- Pin repository: `ipfs pin add -r QmSvmWaRFZp9psEfA5BaVpVR7MKJUtwdoWnN2Qq6PKXTXL`