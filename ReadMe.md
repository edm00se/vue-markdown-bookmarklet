# About

This is a [vue.js](https://vuejs.org/) SPA, mostly just a hasty extension of the [vue.js example](https://vuejs.org/examples/) markdown editor.

## Features

- side-by-side editing and preview
- saving of files as markdown (defaults to `notepad.md`), via `CTRL+S`/`CMD+S`

## Files

```bash
vue-markdown-bookmarklet
├── ReadMe.md                # this ReadMe
├── bs-config.json           # a config file for browser-sync/lite-server
├── index.html               # SPA version before being stripped down for bookmarklet
└── minified-bookmarklet.js  # the bookmarklet

0 directories, 4 files
```

## Install

To 'install', create a new bookmark/favorite, edit the bookmark, set the URL as the contents of the `minified-bookmarklet.js` file, and rename the title of the bookmark appropriately.

## Why?

This is a bit of a silly effort, which was really to just force myself to work through client-side file saving, as a given MIME type. It requires connectivity to CDNJS to work (or at least have a cached copy in the browser), so it's not exactly foolproof.

## License

MIT
