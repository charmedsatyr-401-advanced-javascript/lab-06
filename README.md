![CF](http://i.imgur.com/7v5ASc8.png) LAB
=================================================

## Bitmap Transformer

### Author: Joseph Wolfe

### Links and Resources
* [PR](https://github.com/charmedsatyr-401-advanced-javascript/simple-api/pull/1)

#### Documentation
* [swagger](docs/openapi.json)

### Modules
N/A

##### Exported Values and Methods
`./data/db.json`

###### Commands run to build records in `data/db.json`
`echo '{"name":"electronics", "display_name":"Electronics","description":"Things you plug in."}' | http :3000/categories`
`echo '{"name":"fruit", "display_name":"Fruit","description":"Sweet plant bits you eat."}' | http :3000/categories`
`echo '{"name":"radio", "display_name":"RadioMAX","description":"It is too loud.", "category": "electronics"}' | http :3000/products`
`echo '{"name":"strawberry", "display_name":"Juicy, red strawberry","description":"It tastes so good!", "category": "fruit"}' | http :3000/products`
`echo '{"name":"banana", "display_name":"Big Panamanian banana","description":"It is yellow and curvy.", "category": "fruit"}' | http :3000/products`

#### Running the app
* `json-server --watch data/db.json --id=_id`
* Ensure `json-server` is running on port 3000.
* Navigate to `https://codesandbox.io/s/j29j15x2q9`
* Categories and their corresponding products should display:
  * `electronics` -> `radio`
  * `fruit` -> `strawberry`, `banana`

#### Tests
* How do you run tests?
N/A
* What assertions were made?
N/A
* What assertions need to be / should be made?
The Swagger documentation is imperfect.

#### UML
N/A
