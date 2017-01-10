# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    That is where the routing is done. Defining routes and such.
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember g route campus/boston [options]
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
    {{#link-to 'campus.boston'}}LEENK TO BOSTON{{link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
    The first the way you would reference each in say a template would be different (referencing siblings rather than siblings).
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
      this.get('movies').findRecord('movie', 123);
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    In the pervious example it would look something like
  ```html
    {{#each movies as |movie|}}
    <h3>{{movie.title}}</h3>
    <h3>{{movie.rating}}</h3>
    <h3>{{movie.length}}</h3>
    {{/each}}
```
    ```
