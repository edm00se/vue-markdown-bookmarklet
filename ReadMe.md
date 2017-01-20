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

Alternatively, drag the following link to your bookmarks/favorites bar:

<a href="data:text/html, <html><head><meta charset='utf-8'><title>MD Editor | Web Notepad</title><style type='text/css'>html, body, #editor {margin: 0 auto;height: 100%;font-family: 'Helvetica Neue', Arial, sans-serif;color: #333;} * {-webkit-transition: all linear 1s;} body {padding:2rem;} .label-row {width: 100%;display: block;border-bottom: 1px solid #4e4e4e;} .label-row span {width: 49%;display: inline-block;color: #4e4e4e;text-align: center;} textarea, #editor div {display: inline-block;width: 49%;height: 100%;vertical-align: top;-webkit-box-sizing: border-box;-moz-box-sizing: border-box;box-sizing: border-box;padding: 0 20px;} textarea {border: none;border-right: 1px solid #ccc;resize: none;outline: none;background-color: #f6f6f6;font-size: 14px;font-family: 'Monaco', courier, monospace;padding: 20px;} code {color: #f66;}</style></head><body><div id='editor'><textarea id='sourceMd' v-model='input' debounce='300'></textarea><div v-html='input | marked'></div></div><a download='notepad.md' id='downloadlink' style='display: none'>Download</a><script type='text/javascript' src='https://cdnjs.cloudflare.com/ajax/libs/marked/0.3.2/marked.min.js'></script><script type='text/javascript' src='https://cdnjs.cloudflare.com/ajax/libs/vue/1.0.24/vue.min.js'></script><script type='text/javascript'>var textFile = null,makeTextFile = function (text) {var data = new Blob([text], {type: 'text/markdown'});if (textFile !== null) {window.URL.revokeObjectURL(textFile);}textFile = window.URL.createObjectURL(data);return textFile;};var create = document.getElementById('create'),textbox = document.getElementById('sourceMd');document.addEventListener('keydown', function(e) {if (e.keyCode == 83 && (navigator.platform.match('Mac') ? e.metaKey : e.ctrlKey)) {e.preventDefault();var link = document.getElementById('downloadlink');link.href = makeTextFile(textbox.value);link.click();}}, false);marked.setOptions({renderer: new marked.Renderer(),gfm: true,tables: true,breaks: false,pedantic: false,sanitize: true,smartLists: true,smartypants: false});var vm = new Vue({el: '#editor',data: {input: '# Hasty MD Notepad'},filters: {marked: marked}});</script>">vue md notepad</a>

## Why?

This is a bit of a silly effort, which was really to just force myself to work through client-side file saving, as a given MIME type. It requires connectivity to CDNJS to work (or at least have a cached copy in the browser), so it's not exactly foolproof.

## License

MIT
