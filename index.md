---
layout: page
title: '1. Select a Manifest'
manifests: [ copperfield, bnf640, haemisphaerium ]
loaded_manifest: copperfield
---
<script src="https://use.fontawesome.com/884e80fbb8.js"></script>
<div id="1" style="position:absolute;top:0px;"></div>

Sample pre-loaded annotations can be viewed by toggling the <i class="fa fa-comments" aria-hidden="true"></i> button on the top left of the viewer.

{% include iiif_presentation.html %}

Switch between objects by clicking <i class="fa fa-th-large"></i> in the top left corner, followed by Replace Object <i class="fa fa-refresh"></i>.

<div id="2"></div>
<h1 class="h0">2. Add Annotations</h1>
<br>
<div class="col-4 sm-width-full border-top-thin"></div>
<br>

Make sure you are on Image View <i class="fa fa-photo"></i> then toggle the Annotation <i class="fa fa-comments"></i> panel.

Add one or more annotations to one or more pages.

<div id="3"></div>
<h1 class="h0">3. View Annotations</h1>

To view annotations, visit the SimpleAnnotationStore server: [http://localhost:8888/annotation/](http://localhost:8888/annotation/).

To view the annotation list for a given canvas, Mirador uses a url like this:

```http://localhost:8888/annotation/search?uri=https%3A%2F%2Fderivativo-3.library.columbia.edu%2Fiiif%2F2%2Fpresentation%2F10.7916%2Fd8-fcng-k085%2Fcanvas%2F10.7916%2Fd8-dg2m-rw91&APIKey=user_auth&media=image&limit=10000&_=1570049878385```

The URI in that search is

```https://derivativo-3.library.columbia.edu/iiif/2/presentation/10.7916/d8-fcng-k085/canvas/10.7916/d8-dg2m-rw91```, which is the ```@id``` of this canvas in the source manifest.

The SimpleAnnotationServer documentation has further information on its [search service](https://github.com/glenrobson/SimpleAnnotationServer/blob/master/doc/IIIFSearch.md).

If you have an external annotation server that you would like to use, edit the Mirador configuration in ```_includes/iiif_presentation.html``` to point to it.