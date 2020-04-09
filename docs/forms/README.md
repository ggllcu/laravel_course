# Forms

## The seven restful controller actions

Is a common convention to use this list of methods for a model:
- `index()`: list of all items
- `show()`: shows details of one item
- `create()`: shows a view to create an item
- `store()`: persists an item from request
- `edit()`: shows a view to edit
- `update()`: updates an existing item from a request
- `destroy()`: deletes an item

In Laravel, you can create a controller with all these rooted already set:

```php artisan make:controller ItemsController -r```

In addition, you can also generate a related model by adding the `-m` flag.
In this case, the object model will be passed as argument to the controller methods.

## Restful routing

There is a common convention about routing: __try not to use verbs!__
Instead, you shoud use HTTP verbs.

- `GET /items` -> @index
- `GET /items/create` -> @create
- `POST /items` -> @store
- `GET /items/:id` -> @show
- `GET /items/:id/edit` -> @edit
- `PUT /items/:id ` -> @update
- `DELETE /items/:id` -> @destroy
