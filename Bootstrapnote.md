# Bootstrap

**Bootstrap** is the most popular **CSS Framework** for developing responsive and mobile-first websites.

Get started by including Bootstrap’s production-ready CSS and JavaScript via CDN without the need for any build steps

- Bootstrap includes HTML and CSS based design templates for typography, forms, buttons, tables, navigation, modals, image carousels and many other, as well as optional JavaScript plugins
- Bootstrap also gives you the ability to easily create responsive designs

As reference, here are our primary CDN links.

| Description | URL |
| --- | --- |
| CSS | https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css |
| JS | https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/js/bootstrap.bundle.min.js |

# Use of Bootstrap?

- **Easy to use:** Anybody with just basic knowledge of HTML and CSS can start using Bootstrap
- **Responsive features:** Bootstrap's responsive CSS adjusts to phones, tablets, and desktops
- **Mobile-first approach:** In Bootstrap, mobile-first styles are part of the core framework
- **Browser compatibility:** Bootstrap 5 is compatible with all modern browsers (Chrome, Firefox, Edge, Safari, and Opera). **Note** that if you need support for IE11 and down, you must use either BS4 or BS3.

Bootstrap 5 is designed to be responsive to mobile devices. Mobile-first styles are part of the core framework.

To ensure proper rendering and touch zooming, add the following `<meta>` tag inside the `<head>` element:

> <meta name="viewport" content="width=device-width, initial-scale=1">
> 

The `width=device-width` part sets the width of the page to follow the screen-width of the device (which will vary depending on the device).

The `initial-scale=1` part sets the initial zoom level when the page is first loaded by the browser.

### Bootstrap File Structure

bootstrap/ ├── css/ │ ├── bootstrap.css │ ├── bootstrap.min.css ├── js/ │ ├── bootstrap.js │ ├── bootstrap.min.js ├── img/ │ ├── glyphicons-halflings.png │ ├── glyphicons-halflings-white.png └── [README.md](http://readme.md/) The Bootstrap download includes three folders: css, js, and img. For simplicity, add these to the root of your project. Minified versions of the CSS and JavaScript are also included. It is not necessary to include both the uncompressed and the minified versions.

### What Bootstrap Package Includes?

1. **Scaffolding**: Bootstrap provides a basic structure with Grid System, link styles, background. This is is covered in detail in the section Bootstrap Basic Structure
2. **CSS**: Bootstrap comes with feature of global CSS settings, fundamental HTML elements styled and enhanced with extensible classes, and an advanced grid system. This is covered in detail in the section Bootstrap with CSS.
3. **Components**: Bootstrap contains over a dozen reusable components built to provide iconography, dropdowns, navigation, alerts, popovers, and much more. This is covered in detail in the section Layout Components.
4. **JavaScript Plugins**: Bootstrap contains over a dozen custom jQuery plugins. You can easily include them xall, or one by one. This is covered in details in the section Bootstrap Plugins.
5. **Customize**: You can customize Bootstrap's components, LESS variables, and jQuery plugins to get your very own version.

### Setup

Bootstrap needs at least 3 files for its operation which can be downloaded from the Bootstrap website.

• bootstrap.css : This file contains various CSS for bootstrap. 

• bootstrap.js : This file contains various JavaScript functionalities e.g. dropdown and alerts etc.

 • jQuery.js : This file is the jQuery library which can be downloaded from the ‘jQuery’ website. It is required for proper working of ‘bootstrap.js’.

### Download and include files

<title>Bootstrap Tutorial</title> <script src="asset/js/jquery-3.3.1.min.js"></script> <script src="asset/js/bootstrap.min.js"></script>

## Breakpoint

> Breakpoints are customizable widths that determine how your responsive layout behaves across device or viewport sizes in Bootstrap.
> 
- **Concepts**
    - breakpoints are the building blocks of responsive design.
    - use media queries to architect your CSS by breakpoint.
    - Mobile first, responsive design is the goal

```
$grid-breakpoints: (
  xs: 0,
  sm: 576px,
  md: 768px,
  lg: 992px,
  xl: 1200px,
  xxl: 1400px
);

```

## Container

> Containers are a fundamental building block of Bootstrap that contain, pad, and align your content within a given device or viewport.
> 

bootstrap comes with three different containers:

- `.container`, which sets a `max-width` at each responsive breakpoint
- `.container-{breakpoint}`, which is `width: 100%` until the specified breakpoint
- `.container-fluid`, which is `width: 100%` at all breakpoints

Bootstrap compiled files include :

- Compiled and minified CSS bundles. it is a Sass file which provides additional features such as variables, nesting, mixing, and functions, which make it easier to write and maintain CSS code. It allows for reusable styles, easier management of color schemes and typography, and more flexible and modular stylesheets.
- Compiled and minified JavaScript plugins

Break points in bootstrap are the following:

| Breakpoint | Class infix | Dimensions |
| --- | --- | --- |
| Extra small | None | <576px |
| Small | sm | ≥576px |
| Medium | md | ≥768px |
| Large | lg | ≥992px |
| Extra large | xl | ≥1200px |
| Extra extra large | xxl | ≥1400px |

containers are used to create a consistent and centered layout for the content of a web page. They provide a way to control the width and responsiveness of the page content within a fixed or fluid container.

There are two types of containers in Bootstrap: **`.container`** and **`.container-fluid`**.

1. **`.container`**: This class creates a fixed-width container that adapts its width based on the viewport size. The content inside a **`.container`** is centered horizontally on the page. It has predefined maximum widths for different breakpoints, ensuring that the layout remains responsive.
2. **`.container-fluid`**: This class creates a full-width container that spans the entire width of the viewport. The content inside a **`.container-fluid`** extends to the edges of the screen. It adjusts its width dynamically as the viewport size changes.
3. *` .container-{breakpoint}, which is width: 100% until the specified breakpoint. Break points are the break point of the above

### *Default Containers*

*Our default `.container` class is a responsive, fixed-width container, meaning its `max-width` changes at each breakpoint.*

*`<div class="container">
  <!-- Content here -->
</div>`*

## **Navbar**

Navbars come with built-in support for a handful of sub-components.

- `navbar-brand` for your company, product, or project name.
- `.navbar-nav` for a full-height and lightweight navigation (including support for dropdowns).
- `.navbar-toggler` for use with our collapse plugin and other [navigation toggling](https://getbootstrap.com/docs/5.3/components/navbar/#responsive-behaviors) behaviors.
- Flex and spacing utilities for any form controls and actions.
- `.navbar-text` for adding vertically centered strings of text.
- `.collapse.navbar-collapse` for grouping and hiding navbar contents by a parent breakpoint.
- Add an optional `.navbar-scroll` to set a `max-height` and [scroll expanded navbar content](https://getbootstrap.com/docs/5.3/components/navbar/#scrolling).

```jsx
<nav class="navbar navbar-expand-lg bg-body-tertiary">
<div class="container-fluid">
<a class="navbar-brand" href="#">Navbar</a>
<button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
<span class="navbar-toggler-icon"></span>
</button>
<div class="collapse navbar-collapse" id="navbarSupportedContent">
<ul class="navbar-nav me-auto mb-2 mb-lg-0">
<li class="nav-item">
<a class="nav-link active" aria-current="page" href="#">Home</a>
</li>
<li class="nav-item">
<a class="nav-link" href="#">Link</a>
</li>
<li class="nav-item dropdown">
<a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
Dropdown
</a>
<ul class="dropdown-menu">
<li><a class="dropdown-item" href="#">Action</a></li>
<li><a class="dropdown-item" href="#">Another action</a></li>
<li><hr class="dropdown-divider"></li>
<li><a class="dropdown-item" href="#">Something else here</a></li>
</ul>
</li>
<li class="nav-item">
<a class="nav-link disabled">Disabled</a>
</li>
</ul>
<form class="d-flex" role="search">
<input class="form-control me-2" type="search" placeholder="Search" aria-label="Search">
<button class="btn btn-outline-success" type="submit">Search</button>
</form>
</div>
</div>
</nav>
```

You can replace the text within the `.navbar-brand` with an `<img>`.

```jsx
<nav class="navbar bg-body-tertiary">
<div class="container">
<a class="navbar-brand" href="#">
<img src="/docs/5.3/assets/brand/bootstrap-logo.svg" alt="Bootstrap" width="30" height="24">
</a>
</div>
</nav>
```

## Bootstrap grid

the bootstrap grid divide our container in to 12 equal columns And we can use the prefixes of the above containers to make our columns more responsive on different screen and sizes. we use all types of container for grid parent and then use .col classes to make divide the container in to needed sizes. we can also use prefixes of the container to make it responsive

### Columns

1. **`col`**: This is a generic column class that can be used for creating equal-width columns.
2. **`col-{breakpoint}-{number}`**: This class is used to create columns of specific width based on the specified breakpoint. For example, **`col-sm-4`** creates a column that occupies 4 units of the grid on small screens and above.
3. **`col-{breakpoint}-auto`**: This class creates a column that automatically adjusts its width based on the content within it.
4. **`col-{breakpoint}-offset-{number}`**: This class is used to offset columns horizontally by the specified number of units at the specified breakpoint.

### Gutters

are used to give space between grid columns horizontally and vertically

`.gx-*` classes can be used to control the horizontal gutter widths.

`.gy-*` classes can be used to control the vertical gutter widths within a row when columns wrap to new lines

## Bootstrap helper class

1. Text Alignment:
    - **`.text-left`**: Aligns text to the left.
    - **`.text-center`**: Centers text horizontally.
    - **`.text-right`**: Aligns text to the right.
    - **`.text-justify`**: Justifies text with consistent spacing.
2. Display and Visibility:
    - **`.d-none`**: Hides an element.
    - **`.d-block`**: Makes an element a block-level element.
    - **`.d-inline`**: Makes an element an inline-level element.
    - **`.d-inline-block`**: Makes an element an inline-block level element.
    - **`.invisible`**: Hides an element but preserves its layout.
3. Spacing and Margin:
    - **`.m-{size}`**: Adds margin to all sides of an element (e.g., **`.m-2`** adds margin of 0.5rem).
    - **`.mt-{size}`**: Adds margin to the top of an element.
    - **`.mr-{size}`**: Adds margin to the right of an element.
    - **`.mb-{size}`**: Adds margin to the bottom of an element.
    - **`.ml-{size}`**: Adds margin to the left of an element.
4. Padding:
    - **`.p-{size}`**: Adds padding to all sides of an element.
    - **`.pt-{size}`**: Adds padding to the top of an element.
    - **`.pr-{size}`**: Adds padding to the right of an element.
    - **`.pb-{size}`**: Adds padding to the bottom of an element.
    - **`.pl-{size}`**: Adds padding to the left of an element.
5. Text Formatting:
    - **`.text-uppercase`**: Converts text to uppercase.
    - **`.text-lowercase`**: Converts text to lowercase.
    - **`.text-capitalize`**: Capitalizes the first letter of each word in text.
6. Background Colors:
    - **`.bg-{color}`**: Adds a background color to an element (e.g., **`.bg-primary`** adds the primary color background).
7. Border:
    - **`.border`**: Adds a border to an element.
    - **`.rounded`**: Applies rounded corners to an element.
    - **`.border-{side}`**: Adds a border to a specific side of an element (e.g., **`.border-top`** adds a border to the top side).
    
    # **Bootstrap Text Colors**
    
    This text is muted.
    This text is important.
    This text indicates success.
    This text represents some information.
    This text represents a warning.
    This text represents danger.
    
    ```html
    <div class="container">
      <p class="text-muted">This text is muted.</p>
      <p class="text-primary">This text is important.</p>
      <p class="text-success">This text indicates success.</p>
      <p class="text-info">This text represents some information.</p>
      <p class="text-warning">This text represents a warning.</p>
      <p class="text-danger">This text represents danger.</p>
    </div><div class="container">
      <p class="text-muted">This text is muted.</p>
      <p class="text-primary">This text is important.</p>
      <p class="text-success">This text indicates success.</p>
      <p class="text-info">This text represents some information.</p>
      <p class="text-warning">This text represents a warning.</p>
      <p class="text-danger">This text represents danger.</p>
    </div>
    
    ****
    ```
    
    # **Bootstrap Columns**
    
    Three equal-width columns, on all devices and screen widths:
    **Example**
    
    `<div class="row">
      <div class="col">.col</div>
      <div class="col">.col</div>
      <div class="col">.col</div>
    </div>`
    
    **Responsive Columns**
    Three equal-width columns scaling to stack on top of each other on small screens:
    **Example**
    
    `<div class="row">
      <div class="col-sm-4">.col-sm-4</div>
      <div class="col-sm-4">.col-sm-4</div>
      <div class="col-sm-4">.col-sm-4</div>
    </div>`
    
    **What is Responsive Web Design?**
    
    Responsive web design is about creating web sites which automatically adjust themselves to look good on all devices, from small phones to large desktops.
    
    <title>Bootstrap Example</title> <script src="[
    
    ```css
    [https://ajax.googleapis.com/ajax/libs/jquery/3.6.4/jquery.min.js](https://ajax.googleapis.com/ajax/libs/jquery/3.6.4/jquery.min.js)"></script>](https://ajax.googleapis.com/ajax/libs/jquery/3.6.4/jquery.min.js](https://ajax.googleapis.com/ajax/libs/jquery/3.6.4/jquery.min.js)%22%3E%3C/script%3E)
    ```
    
    ```css
    [https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js](https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js)"></script>](https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js](https://maxcdn.bootstrapcdn.com/bootstrap/3.4.1/js/bootstrap.min.js)%22%3E%3C/script%3E)
    ```
    
    ### ***Responsive containers***
    
    *Responsive containers allow you to specify a class that is 100% wide until the specified breakpoint is reached, after which we apply `max-width`s for each of the higher breakpoints. For example, `.container-sm` is 100% wide to start until the `sm` breakpoint is reached, where it will scale up with `md`, `lg`, `xl`, and `xxl`.*
    
    *`<div class="container-sm">100% wide until small breakpoint</div>
    <div class="container-md">100% wide until medium breakpoint</div>
    <div class="container-lg">100% wide until large breakpoint</div>
    <div class="container-xl">100% wide until extra large breakpoint</div>
    <div class="container-xxl">100% wide until extra extra large breakpoint</div>`*
    
    Grid to build layouts of all shapes and sizes thanks to a twelve column system..
    
    Bootstrap’s grid system uses a series of containers, rows, and columns to layout and align content. It’s built with [flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox) and is fully responsive.
    
    # **Bootstrap Tables**
    
    You can create tables with basic styling that has horizontal dividers and small cell padding (8px by default), by just adding the Bootstrap's class `.table` to the `[<table>](https://www.tutorialrepublic.com/html-reference/html-table-tag.php)` element.
    
    ****Example****
    
    ```markup
    <table class="table"><thead><tr><th>#</th><th>First Name</th><th>Last Name</th><th>Email</th></tr></thead><tbody><tr><td>1</td><td>Clark</td><td>Kent</td><td>clarkkent@mail.com</td></tr><tr><td>2</td><td>Peter</td><td>Parker</td><td>peterparker@mail.com</td></tr><tr><td>3</td><td>John</td><td>Carter</td><td>johncarter@mail.com</td></tr></tbody></table>
    ```
    
    # Bootstrap basic classes
    
    Bootstrap provides a set of basic classes that you can use to style your website quickly and easily. These classes include typography, colors, spacing, and display utilities.
    
    Here are some examples of Bootstrap classes:
    
    - `btn`: Used for styling buttons
    - `form-control`: Used for styling form inputs like textboxes and dropdowns
    - `img-fluid`: Used for making images responsive within their container
    - `alert`: Used for displaying alert messages
    - `card`: Used for creating content containers with various styles and layouts
    ****
    
    # **Bootstrap Alerts**
    
    Bootstrap provides an easy way to create predefined alert messages:
    **Success!**  This alert box indicates a successful or positive action.
    **Warning!**  This alert box indicates a warning that might need attention.
    **Danger!**  This alert box indicates a dangerous or potentially negative action.
    **Primary!**  This alert box indicates an important action.
    **Example**
    
    `<div class="alert alert-success">
      <strong>Success!</strong> Indicates a successful or positive action.
    </div>
    <div class="alert alert-warning">
      <strong>Success!</strong> Indicates a successful or positive action.
    </div>
    <div class="alert alert-danger">
      <strong>Success!</strong> Indicates a successful or positive action.
    </div>
    <div class="alert alert-primary">
      <strong>Success!</strong> Indicates a successful or positive action.
    </div>`
    ****
    
    # **Bootstrap Buttons**
    
    Bootstrap provides different styles of buttons:
    Basic :  Primary Secondary Success Info Warning Danger Dark
    **Example**
    
    `<button type="button" class="btn">Basic</button>
    <button type="button" class="btn btn-primary">Primary</button>
    <button type="button" class="btn btn-secondary">Secondary</button>
    <button type="button" class="btn btn-success">Success</button>
    <button type="button" class="btn btn-info">Info</button>
    <button type="button" class="btn btn-warning">Warning</button>
    <button type="button" class="btn btn-danger">Danger</button>
    <button type="button" class="btn btn-dark">Dark</button>`
    
    # **Form controls**
    
    Give textual form controls like `<input>`s and `<textarea>`s an upgrade with custom styles, sizing, focus states, and more.
    
    ```jsx
    <div class="mb-3">
    <label for="exampleFormControlInput1" class="form-label">Email address</label>
    <input type="email" class="form-control" id="exampleFormControlInput1" [placeholder="name@example.com](mailto:placeholder=%22name@example.com)">
    </div>
    <div class="mb-3">
    <label for="exampleFormControlTextarea1" class="form-label">Example textarea</label>
    <textarea class="form-control" id="exampleFormControlTextarea1" rows="3"></textarea>
    </div>
    ```
    
    # **Bootstrap Cards**
    
    **John Doe**
    Some example text some example text. John Doe is an architect and engineer.
    **Example**
    
    `<div class="card" style="width:400px">
      <img src="img_avatar1.png" alt="Card image">
      <div class="card-body">
        <h4 class="card-title">John Doe</h4>
        <p class="card-text">Some example text.</p>
        <a href="#" class="btn btn-primary">See Profile</a>
      </div>
    </div>`
    ****
    
    # Customizing Bootstrap
    
    While Bootstrap provides a great set of default styles and components, you may want to customize them to fit your specific needs. Bootstrap provides a variety of customization options, including Sass variables, mixins, and themes.
    
    1. **`container`**: This class is used to create a fixed-width container that horizontally centers your site's content. It provides a responsive layout by adapting to different screen sizes.
    2. **`row`**: The **`row`** class is used to create a horizontal row within a container. It is used in conjunction with columns (**`col-*`** classes) to create a grid-based layout for organizing content.
    3. **`col-*`**: The **`col-*`** classes are used to define the columns within a row. They provide a responsive grid system, allowing you to specify different column widths for different screen sizes. For example, **`col-md-6`** creates a column that takes up half of the available width on medium-sized screens.
    4. **`btn`**: The **`btn`** class is used to create stylish buttons. It provides pre-defined styles for different button types, such as primary, secondary, success, warning, etc. You can also combine **`btn`** with other classes to create button variations, such as **`btn-lg`** for a large button or **`btn-block`** to make the button span the full width of its container.
    5. **`alert`**: The **`alert`** class is used to display informative or warning messages to the user. It provides different contextual styles, such as success, warning, danger, etc., and can be used with icons and dismissible functionality.
    6. **`navbar`**: The **`navbar`** class is used to create a responsive navigation bar. It provides pre-defined styles and layout options for creating a navigation menu that collapses into a toggleable mobile menu on smaller screens.
    7. **`card`**: The **`card`** class is used to create flexible and stylish content containers, often used for displaying information, products, or articles. It allows you to create a consistent card layout with options for headers, footers, images, and various content arrangements.
    8. **`modal`**: The **`modal`** class is used to create pop-up modal windows that display additional content or require user interaction. Modals can be triggered by buttons or links and are useful for displaying forms, images, messages, or other content without navigating away from the current page.
    9. **`carousel`**: The **`carousel`** class is used to create image sliders or carousels. It enables you to display a set of images or content in a rotating manner, with navigation controls to switch between slides manually or automatically.
    10. **`badge`**: The **`badge`** class is used to create small, informative notifications or indicators. It can be applied to elements such as buttons, links, or labels to display numbers or status labels. Badges are commonly used for displaying unread message counts, notification counts, or status indicators. The following is a basic structure of a Bootstrap grid:
    
    First; create a row (`<div class="row">`). Then, add the desired number of columns (tags with appropriate `.col-*-*` classes). Note that numbers in `.col-*-*` should always add up to 12 for each row.
    
    # **Nesting**
    
    To nest your content with the default grid, add a new `.row` and set of `.col-sm-*` columns within an existing `.col-sm-*` column. Nested rows should include a set of columns that add up to 12 or fewer (it is not required that you use all 12 available columns).
    
    ```
    <div class="container text-center">
      <div class="row">
        <div class="col-sm-3">
          Level 1: .col-sm-3
        </div>
        <div class="col-sm-9">
          <div class="row">
            <div class="col-8 col-sm-6">
              Level 2: .col-8 .col-sm-6
            </div>
            <div class="col-4 col-sm-6">
              Level 2: .col-4 .col-sm-6
            </div>
          </div>
        </div>
      </div>
    </div>
    ```
    
    ## **Columns**
    
    ### **Alignment**
    
    - **Vertical alignment**
    
    Change the vertical alignment with any of the responsive `align-items-*` classes.
    
    Example
    
    ```
    <div class="container text-center">
      <div class="row align-items-start">
        <div class="col">
          One of three columns
        </div>
        <div class="col">
          One of three columns
        </div>
        <div class="col">
          One of three columns
        </div>
      </div>
    </div>
    ```
    
    Or, change the alignment of each column individually with any of the responsive `.align-self-*` classes.
    
    Example
    
    ```
    <div class="container text-center">
      <div class="row">
        <div class="col align-self-start">
          One of three columns
        </div>
        <div class="col align-self-center">
          One of three columns
        </div>
        <div class="col align-self-end">
          One of three columns
        </div>
      </div>
    </div>
    ```
    
    - **Horizontal alignment**
    
    Change the horizontal alignment with any of the responsive `justify-content-*` classes.
    
    Example
    
    ```
    <div class="container text-center">
      <div class="row justify-content-start">
        <div class="col-4">
          One of two columns
        </div>
        <div class="col-4">
          One of two columns
        </div>
      </div>
      <div class="row justify-content-center">
        <div class="col-4">
          One of two columns
        </div>
        <div class="col-4">
          One of two columns
        </div>
      </div>
      <div class="row justify-content-end">
        <div class="col-4">
          One of two columns
        </div>
        <div class="col-4">
          One of two columns
        </div>
      </div>
      <div class="row justify-content-around">
        <div class="col-4">
          One of two columns
        </div>
        <div class="col-4">
          One of two columns
        </div>
      </div>
      <div class="row justify-content-between">
        <div class="col-4">
          One of two columns
        </div>
        <div class="col-4">
          One of two columns
        </div>
      </div>
      <div class="row justify-content-evenly">
        <div class="col-4">
          One of two columns
        </div>
        <div class="col-4">
          One of two columns
        </div>
      </div>
    </div>
    ```
    
    ### **Column breaks**
    
    Breaking columns to a new line in flexbox requires a small hack: add an element with `width: 100%` wherever you want to wrap your columns to a new line. Normally this is accomplished with multiple `.row`s, but not every implementation method can account for this.
    
    Example
    
    ```
    <div class="container text-center">
      <div class="row">
        <div class="col-6 col-sm-3">.col-6 .col-sm-3</div>
        <div class="col-6 col-sm-3">.col-6 .col-sm-3</div>
    
        <!-- Force next columns to break to new line -->
        <div class="w-100"></div>
    
        <div class="col-6 col-sm-3">.col-6 .col-sm-3</div>
        <div class="col-6 col-sm-3">.col-6 .col-sm-3</div>
      </div>
    </div>
    
    ```
    
    ### **Order classes**
    
    Use `.order-` classes for controlling the **visual order** of your content. These classes are responsive, so you can set the `order` by breakpoint (e.g., `.order-1.order-md-2`).
    
    Example
    
    ```
    <div class="container text-center">
      <div class="row">
        <div class="col">
          First in DOM, no order applied
        </div>
        <div class="col order-5">
          Second in DOM, with a larger order
        </div>
        <div class="col order-1">
          Third in DOM, with an order of 1
        </div>
      </div>
    </div>
    ```
    
    There are also responsive `.order-first` and `.order-last` classes that change the `order` of an element by applying `order: -1` and `order: 6`, respectively
    
    Example
    
    ```
    <div class="container text-center">
      <div class="row">
        <div class="col order-last">
          First in DOM, ordered last
        </div>
        <div class="col">
          Second in DOM, unordered
        </div>
        <div class="col order-first">
          Third in DOM, ordered first
        </div>
      </div>
    </div>
    ```