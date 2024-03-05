# Bootstrap 5 Tutorial

The original source can be found in the [link](https://www.youtube.com/watch?v=4sosXZsdy-s&t=182s)

This crash course will contain navbar, smooth scrolling, showcase area, css grid, bootstrap icons, acordian, cards, contact info and map box, model for form, hamburger menu.

## Quick Introduction to BS5

This set of CSS class, or we can say CSS Framework with predefined CSS Classes. The Bootstrap 5 can be overriden for desired CSS attributes like color forexample. But, it requires sass override which will not be shown in the tutorial but it can be handled anywhere else.<br>
In order to fully work with Bootstrap5, the both CSS and JS bundle need to be imported.

```html
<!-- Importing CSS in head -->
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">

<!-- importing JS in last part in body -->
<script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.8/dist/umd/popper.min.js" integrity="sha384-I7E8VVD/ismYTF4hNIPjVp/Zjvgyol6VFvRkX/vR+Vc4jQkC+hVqc2pM8ODewa9r" crossorigin="anonymous"></script>
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.min.js" integrity="sha384-0pUGZvbkm6XF6gxjEnlmuGrJXVbNuzT9qBBavbLwCsOGabYfZo0T0to5eqruptLy" crossorigin="anonymous"></script>
```

## Starting with Navbar

Navbar can be used with nav tag including _navbar_ classes.

__navbar-expang-lg__ : This is allows to navbar shown until hit the large breakpoint being hit. Until then it will show expand. After the part, it will be hamburger menu.<br>
__navbar-dark__ : This will make the navbar texts lighter since the navbar is used as dark with the tag __bg-dark__.<br>
Adding navbar items under div.container since it will have container structure in navbar. Just the use case. So the use case is shown in here.

```html
<nav class="navbar">
    <div class="container">
        <a href="#" class="navbar-brand">Test</a>
        <div class="collapse navbar-collapse">
            <ul class="navbar-nav">
                <li class="nav-item">
                    <a href="#item1" class="nav-link">item1</a>
                </li>
                <li class="nav-item">
                    <a href="#item2" class="nav-link">item2</a>
                </li>
                <li class="nav-item">
                    <a href="#item3" class="nav-link">item3</a>
                </li>
            </ul>
        </div>
    </div>
</nav>
```

From here we can understand that, navbar-brand is used for Brand about website.<br>
collapse & navbar-collapse is used for collapsing items for each navbar item that can be accessible.<br>
navbar-nav, this is navbar navigation item that will be used in unordered list.<br>
nav-item is used for each item that will be listed in navbar.

There is another class is used in ul _ms-auto_ which stands for margin start is auto. This will make the menu items can be disapear in navbar for hitbar menu due to navbar-expand-lg class. Thiss wil used for our burger menu.

```html
<button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navmenu" aria-expanded="false">
    <span class="navbar-toggler-icon"></span>
</button>
```

This is the toggler bar with couple attribute. Let's talk quickly eachone for what are they responsible for.

_navbar-toggler_ class is responsible to create hamburger menu.<br>
type button is standard CSS for button creation.<br>
_data-bs-toggle="collapse"_ part is responsible for what the action will be based on given information __collapse__.<br> _data-bs-target_ : This will be give the target item with id. Which in this case navmenu. Which means the items will be toggled in div should have same id with this one. Check the [HTML](/index.html) accordingly.

Later on, we add one class for fixing the navbar at the top with _fixed-top_. But it will make navbar sit on top of picture, to prevent that we wrote small css block

```css
body::before {
    display:block;
    content:'';
    height:60px
}
```

which is adding the 60px ghost element on the top.

## Continue with Showcase

The general informations will be seperated with sections. It will have different classes which is maybe different from previous usages.

pb-1 -> pb-5 : Padding Bottom from 1 to 5. 1 is least pixel padding and 5 is most.
pt-1 -> pt-5 : Padding top from 1 to 5.
px-1 -> px-5 : Padding from both left to right
py-1 -> py-5 : Padding frmo top to botton
p-1 -> p-5 : Padding all around.

_img-fluid_ : is used for make image resize in the div
_d-flex_ : convert the div to flex
_d-sm-flex_ : Make flex convertion until hit the small breakpoint
_text-sm-start_: Text Small Screen margin from start.

## Next Area is News Letter Area, which I don't plan to use that much at all.

## Cards with using Grid structure

In order to use GRID structure from bootstrap you need to wrapped two things.

```html
<div class="row">
    <div class="col"></div>
    <div class="col"></div>
    <div class="col"></div>
</div>
```

This will be divided with rows and columns based on description. Class names are straight-forward. Use cases may seems awkward.

There is a small section for css that will be uses icons with importing css accordingly. More explanation can be found in the [link](https://blog.getbootstrap.com/2021/01/07/bootstrap-icons-1-3-0/)

```html
<!-- Option 1: Include in HTML -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons@1.3.0/font/bootstrap-icons.css">
```

bi and bi-*** tags used for icons which can be imported in i tag.

## Learning Section

This section was pretty straightforward. We didn't use anything that now showed before.

## Accordion / FAQ part

Now, to save time we copy paste the original code but I believe the classes are make sense now

1. created section about question to navigate from navbar
1. div.container
1. Titled with H2
1. accordion & accordion-flush classes to make accordion in one div container. This one has id of accordionFlushExample to wrap I guess
1. accordion-item for each item
    1. accordion-button collapsed classes for make button clickable and collapsed by default. These ones has target of flush-collapseOne, flush-collapseTwo, etc. data-bs-parent="#accordionFlushExample" is the data source for trigger I guess.
    1. div with #flush-collapseOne Two Three to interact with.
    1. div.accordion-body for collapsing application.

## Getting to the end with Instruction page (which has different cards)

Very straightforward again,

1. section with id
1. div.container
    1. h2 for title
    1. p for explanation
    1. grid systems for cards with class row
        1. col
            1. card
                1. card-body

This is somewhat structure in the bootstrap.

## Map Boxes

This map boxes implementation requires a API key to generate map.
in mapbox.com, you need to sign up to generate key.

Include the CDN css and js
you need to open your own script and paste your code, which will be supplied by website with your own API Key.

In your script, you'll add `center[longtitude, latitude]` and `zoom[zoom_index]` with your own desired longtitude and lattitude with zoom index.

then just adding this one in html
```html
<div id="map"></div>
```

After this stage, you'll not able to see map since you didn't give size to the map which will be handled in your own css via

```css
#map {
    width: 100%;
    height: 100%;
    border-radius: 10px;
}
```

## Last part with footer

Again straightforward as usage.

## Modal for registeration.

This modal part will be added to showcase section. So the trigger codes will be following needs to be checked in html.<br>
but remaining model div can be placed in anywhere really.

## END