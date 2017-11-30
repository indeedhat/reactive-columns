### Reactive Columns
A set of css rules to allow for reactive column based layouts.

### Basic Usage
simply add .col-... classes to elements to enable the reactive sizing to your elements\
All .col- elements should be wrapped in a .row element to provide clearfix
```html
<!DOCTYPE html>
<html>
  <head>
    <link rel="reactive-cols.min.css" />
  </head>
  <body>
    <header class="row">
      <img src="logo.png" alt="site logo" class="col-3 col-t-12" />
      <nav class="col-9 col-t-12">
        ...
      </nav>
    </header>
    <main style="row">
      <section id="page-content" class="col-8 col-m-12">
        ...
      </section>
      <aside class="col-4 col-no-mobile">
      
      </aside>
    </main>
    <footer>
      ...
    </footer>
  </body>
</html>
```

### Class groups

in descending order of priority

| Class Group  | Page Width (px) | Device target        |
|--------------|-----------------|----------------------|
| col-[1-12]   | any size        | any device           |
| col-w-[1-12] | > 1920          | wide screen desktops |
| col-d-[1-12] | > 1366          | standard desktops    |
| col-l-[1-12] | > 768           | laptops              |
| col-t-[1-12] | > 600           | tablets              |
| col-m-[1-12] | <= 600          | mobile devices       |

all col- classes excluding col-[1-12] also have a col-no- and col-no- class to provide showing/hiding elements at 
specific screen sizes

finally there is a col-no-float class to be applied to any cols that you wish to arrange without a float

### Box Model
originally this style included a `* {box-sizing:border-box;}` rule to standardise the box model but this can cause issues 
when integrating it into existing code bases so it has been removed.\
I would however highly recommend that you add this in for new projects

### License
[MIT Licensed](./LICENSE)
