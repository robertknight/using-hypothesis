title: Using Hypothesis
author:
	name: Robert Knight
	twitter: "@robknight_"
controls: true
theme: sudodoki/reveal-cleaver-theme
output: index.html

--

# Using Hypothesis

How to use Hypothesis as a user and developer

--

## What can you do with Hypothesis?

* Annotate and discuss web pages
* Share annotations
* Add annotation tools to your own web pages
* Fetch public annotations via the API

--

## Annotate web pages

View and add annotations on any web page using
the Hypothesis sidebar.

Links on the [https://hypothes.is]() homepage.


* Install the [browser extension](https://chrome.google.com/webstore/detail/bjfhmglciegochdpefhhlphglcehbmek)+
* Add the bookmarklet to your browser toolbar 
* Enter the URL you want to annotate at [via.hypothes.is](https://via.hypothes.is)

--

* Go to any web page or PDF
* Click the bookmarklet or extension icon to activate
* Annotate!

--

* Make annotations public, private or shared with a private group
* Add tags, images, lists, code etc. (Supports Markdown and LaTeX equations)
* Reply to others' annotations and get notifications of replies

--

## See what others are annotating

* See all Public and Private annotations at [https://hypothes.is/stream]()
* RSS feed also available
```
https://hypothes.is/stream.rss?uri.parts=bbc
```

--

## Share annotations

* Each annotation has a link that you can share
* Link to an annotated version of any web page:

```
https://via.hypothes.is/<URL>
```

--

## Add Hypothesis to your web pages

You can add Hypothesis to your own web pages.

```
<html>
<head>
	<script>
		window.hypothesisConfig = function () {
			return { showHighlights : true };
		};
	</script>
	<script defer src="https://hypothes.is/embed.js"></script>
</head>
</html>
```

--

### Caveats

* Does not work on local files (with `file:///`) URLs, you'll need
  to serve the app with a simple web server

* If you serve the same content from multiple pages, include a link
  to the main URL.
```
  <link rel="canonical" href="http://yoursite.com/article.html">
```

--

## Get data from Hypothes.is

Hypothesis has an API. Get public annotations for any web page:

```
curl https://hypothes.is/api/search?url=<URL>
```

Search for annotations:

```
curl https://hypothes.is/api/search?any=climate
```

More documentation at [h.readthedocs.org](https://h.readthedocs.org)

--

What else can you do with the API?

* Create, update and delete annotations
* Search by tag etc.
* Get RSS feeds for all annotations on a site

--

## Build your own version of Hypothesis

* You can build and run your own instance. See the [documentation site](https://h.readthedocs.org)
* Open source libraries for anchoring annotations

--

## Links

* [Documentation site](h.readthedocs.org)
* [Github](https://github.com/hypothesis)
* [W3C Web Annotation Working Group](http://www.w3.org/annotation/)
* Twitter - @hypothesis

