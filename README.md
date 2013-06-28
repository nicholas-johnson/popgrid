PopGrid
=======

Responsive Semantic Grid layouts with SASS and no non-sematic classes.

http://www.popgridsass.com

Want easy responsive layouts, but don't like littering your html with non-semantic classes? Me too.

Popgrid is a drop in replacement for Bootstrap's class based non-semantic grid system. It responds, just like Bootstrap.

##A Bootstrap Layout

    <!html>
    <html>
      <head>
      </head>
      <body class="row">
        <article class="span8">
        </article>
        <aside class="span4">
        </aside>
      </body>
    </html>

## The same layout in Popgrid

    <!html>
    <html>
      <head>
      </head>
      <body>
        <article>
        </article>
        <aside>
        </aside>
      </body>
    </html>

    @include 'popgrid;'
    body {
      @include row;
    }
    article {
      @include span(8);
    }
    aside {
      @include span(4);
    }

# Grid Layouts

Are you tired of adding class="span5"? Me too. Popgrid provides row, container, span and offset mixins. Mix them them to your regular SASS declarations and Popgrid will generate responsive CSS which will scale just like Bootstrap.

* row - defines a row in a layout.
* span(x) - tells an element to fill a set number of columns.
* offset(x) - moves an element in a set number of columns from the left.
* container - when you just want content.

# Typography

PopGrid is designed to look nice out of the box. Include popgrid_typography and your page will look nice right away. Change the typography values in popgrid_overrides.scss to tinker with the look.

## page_header

The page_header mixin is a direct replacement for the Bootstrap page-header class.

Bootstrap:

    <div class="page-header">
      <h1>Upsetting non-semantic-ness</h1>
    </div

PopGrid

    <h1>Amazing Semantic Awesomeness!</h1>

    h1 {
      @include page_header;
    }

## Lead copy

The lead mixin lets you do nice, bootstrap style callout headings:

Bootstrap:

    <div class="intro">
      <p class="lead">Some welcome text</p>
    </div>

Popgrid

    <div class="intro">
      <p>Some welcome text</p>
    </div>

    .intro p {
      @include lead
    }

# Configuration

All variables are extracted into the popgrid_overrides.scss file. Make your changes here.

# Triggering responsiveness with Meta Viewport

Be sure to include the meta-viewport element in your header to trigger your responsive layout on mobile devices.

    <meta name="viewport" content="width=device-width, initial-scale=1.0">