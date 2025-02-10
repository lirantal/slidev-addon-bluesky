# slidev-addon-bluesky

[![NPM version](https://img.shields.io/npm/v/slidev-addon-bluesky?color=3AB9D4&label=)](https://www.npmjs.com/package/slidev-addon-bluesky)

Slidev component to integrate with [Bluesky](https://bsky.app/) to render a post in your slides, similar to the [Tweet component](https://sli.dev/builtin/components#tweet).

## Installation

```bash
npm install slidev-addon-bluesky
```

Declare the addon in your front matter of the `slides.md` file:

```md
---
addons:
  - slidev-addon-bluesky
---
```

## Usage

```md
---
layout: default
---

# The following is a Bluesky post

<Bluesky id="at://did:plc:hnlvjno2m7l2kqllgum26bv2/app.bsky.feed.post/3lhr6jiuaqs25" />
```

## Props

- `id`: The full Bluesky post ID (you can grab this from the link to share the post as an embed)


## Author

Liran Tal <liran@lirantal.com>