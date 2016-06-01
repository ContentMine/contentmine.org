This is the contentmine.org website.

It is a simple static website that uses getter to allow for sort-of templating by using dynamic content loading.

Codeship is used so that any commit to the master branch automatically updates the live site.

To keep things neat, it is recommended to put such static content into a folder called /static.

Pages can be created by putting them in the /content folder. The filename shuold be whatever is expected to form the URL, without the /content part.

Content files can include html or markdown. Markdown should be wrapped in opening and closing &lt:markdown&gt; tags.

The usual index.html file naming paradigm can be used inside any folder in the usual way, as the default file to be served if the URL entered matches only the folder name.

For example if the content of this repo is served at mysite.com then a request to mysite.com/my/file will serve the content found in the file at content/my/file.

If mysite.com/content/my is requested, then the content of the file at content/my/index will be served, or else content/my/index.html.

If a file with the given name in the URL cannot be found in the specified folder, and cannot be found with .html appended, and also an index or index.html file cannot be found, 
then the 404 file found in the top level directory will be served instead. If that does not exist, then a standard nginx 404 will occur.

All the content files are requested and served as javascript dynamic requests, to populate a section of the page from which the request is issued.

To edit the paraphernalia of the page, see the index.html, header.html, and footer.html files in the top level directory of this repository.



