![CF](http://i.imgur.com/7v5ASc8.png) LAB
=================================================

## HTTP and REST | Simple API

### Author: Joseph Wolfe

### Links and Resources
* [PR](https://github.com/charmedsatyr-401-advanced-javascript/simple-api/pull/2)
* [front end](https://codesandbox.io/s/j29j15x2q9)

#### Documentation
* [swagger](docs/swagger.json)

### Modules
N/A

##### Exported Values and Methods
`./data/db.json`

###### Commands run to POST records to `./data/db.json`
`echo '{"name":"electronics", "display_name":"Electronics","description":"Things you plug in."}' | http :3000/categories`

`echo '{"name":"fruit", "display_name":"Fruit","description":"Sweet plant bits you eat."}' | http :3000/categories`

`echo '{"name":"radio", "display_name":"RadioMAX","description":"It is too loud.", "category": "electronics"}' | http :3000/products`

`echo '{"name":"strawberry", "display_name":"Juicy, red strawberry","description":"It tastes so good!", "category": "fruit"}' | http :3000/products`

`echo '{"name":"banana", "display_name":"Big Panamanian banana","description":"It is yellow and curvy.", "category": "fruit"}' | http :3000/products`

`echo '{"name":"socks", "display_name":"Socks are fruit","description":"Are socks fruit?.", "category": "fruit"}' | http :3000/products`

###### Commands run to DELETE records from `./data/db.json`
* Above, socks were added to the category `fruit`. This entry to `products` can be deleted using the following syntax, where `ID` is the `_id` of the "socks" entry in `./data/db.json`:

`http delete :3000/products/ID`
* Likewise, a category can be deleted using the following syntax, where `ID` is the `_id` of the category in `./data/db.json`:

`http delete :3000/categories/ID`

It may be necessary to GET an object from the database to ascertain its `_id`.

#### Running the app
* `json-server --watch data/db.json --id=_id`
* Ensure `json-server` is running on port 3000.
* Navigate to `https://codesandbox.io/s/j29j15x2q9`
* Categories and their corresponding products should display when a category is clicked:
  * `electronics` -> `radio`
  * `fruit` -> `strawberry`, `banana`
* If `json-server` is running as indicated, you should be able to make additions or modifications to `./data/db.json` through the `json-server` API or through requests made through the `swagger.io` interface after copying/pasting the documentation at `./docs/swagger.json` into an editor at [https://editor.swagger.io](https://editor.swagger.io).
* Performing `POST` and `DELETE` operations on the command line:
  * POST operations can be made using the following syntax for the `httpie` package on the command line: `echo JSON | http :3000/categories` or `echo JSON | http :3000/products`
  * DELETE operations can be made using the following syntax for the `httpie` package on the command line: `http delete :3000/categories/ID` or `http delete :3000/products/ID`
  * See examples above in the sections "Commands run to POST records to `./data/db.json` and "Commands run to DELETE records from `./data/db.json`.

#### Tests
* How do you run tests?

N/A
* What assertions were made?

N/A
* What assertions need to be / should be made?

N/A

#### UML
N/A
