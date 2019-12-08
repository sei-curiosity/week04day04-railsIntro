# Role: Router

## Can Talk To

- People Controller
- Places Controller
- Things Controller

## Description

The router is responsible for

1. Receiving the requests that the client sends.

1. Triggering the appropriate controller actions in response to those requests
   (using the routes that have been previously configured).

1. Sending the 'view', produced by the controller at the end of its action,
   back to the client.

The table of routes you'll be working with is below; any time a route has a
term with a colon, like `:this`, it means that a value will be passed in as
part of the path.

## Routes for People(/Places/Things) Controller

|     Path      | Request Type |    Controller     | Controller Action |                                    Controller Directions                                     |
|:-------------:|:------------:|:-----------------:|:-----------------:|:--------------------------------------------------------------------------------------------:|
|   `/people`   |     GET      | People Controller |      `index`      |                                    _Retrieve all people._                                    |
|   `/people`   |     POST     | People Controller |     `create`      |                   _Make a new person, using data provided by the request._                   |
| `/people/:id` |     GET      | People Controller |      `show`       |                     _Retrieve the specific person who has the given id._                     |
| `/people/:id` |  PATCH/PUT   | People Controller |     `update`      | _Change the properties of the person with the given id, using data provided by the request._ |
| `/people/:id` |    DELETE    | People Controller |     `destroy`     |                           _Destroy the person with the given id._

## Errors

If for whatever reason you can't successfully complete your job, send an
'ERROR' message back to the client.

For example:

- `HTTP 404/Not Found`
