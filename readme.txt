so _site is the local build of the compiled md and html files
_layouts is like a template that diff static pages can use for styling and html _layout
_includes is for things that are always going to be referred in multiple places so we have single source of truth
_sass is for scss styling

_authors is the folder where declared authors in the collections _config.yml live. So since _config.yml defines a collection of authors, there needs to be an _authors folder in the root along with the _config.yml

if you want jekyll to process a file, always remember to put:
---
---
at the top for the front matter. like for html, css, md, etc

To Build/Run:

run windows installer for ruby, say yes to defaults
create working directory
git init in working directory
run below commands:
bundle init
bundle add webrick as ruby 3 doesn't include webrick which is needed for local dev
bundle add jekyll-watch
bundle add em-websocket (live reload)
bundle add kramdown-parser-gfm (for markdown)
jekyll serve --livereload