# Routing

## Basic Routing and Views

We can think views as the HTML response that we want to show as response to a user request.

You can see all your views inside `resources > views`

They looks very like to normal HTML pages, but the actually are blade file, a template engine for PHP.

```Blade Template => Blade Engine => Php files => HTML response```

## Pass Request Data to Views 

We can take data from the route using the `request` helper function"

```$value = request ($key);```

Then we can use this value and pass it to the view.

```return view('view', ['key' => $value]);```

In the view we can use __Blade__ to access the data:

`{{ $ variable }}` -> this syntax escape the value and then echo.

## Route Wildcards

Wildcards are used when the cate can be variable:

```Route::get('/posts/{slug}', function() );```

Laravel will create a variable with the same name you used in your wildcard, in this case `$slug`.

It's a good idea check in the route if the content exists, otherwise return:

```abort (404, 'Nothing here');```

## Routing to controllers

When we set up a route, instead of returning a view, we can return a controller:

```Route::get('/posts/{slug}', 'controller@method');```
