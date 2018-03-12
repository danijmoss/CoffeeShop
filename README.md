# jQuery Coffee Shop App
A small application using JSON Server to host data displaying incoming orders for a coffee shop. It is a UI addition to the small site created from the tutorial by [LearnCode.Academy](https://www.youtube.com/playlist?list=PLoYCgNOIyGABdI2V8I_SWo22tFpgh2s6_).

The app uses a JSON file to create a local REST API to server the customer data. 

The site is styled with Bootstrap v. 3.3.7 and uses jQuery and AJAX to implement CRUD methods to consume the API and display the data to the user. 

Mustache.js is used to create a template to display the incoming cutomer orders.

# Resources
- [jQuery for Beginners Tutorial Series](https://goo.gl/Fuk4Va)
- [JSON Server](https://github.com/typicode/json-server)
- [Bootstrap](https://getbootstrap.com/docs/3.3/)
- [MustacheJS](https://github.com/janl/mustache.js/)
- [jQuery](https://developers.google.com/speed/libraries/#jquery)

# Installation and Usage
Install json-server
```
$ npm install -g json-server
```

Create a db.json file with some basic data
```
{
  "orders": [
    {
      "id": 1,
      "name": "Jane",
      "drink": "Americano w/ Creme",
      "snack": "",
      "special": "Biscotti"
    },
    {
      "id": 2,
      "name": "Bob",
      "drink": "Hot Chocolate",
      "snack": "Cookie",
      "special": ""
      },
    {
      "id": 3,
      "name": "Louis",
      "drink": "Cappuccino",
      "snack": "Scone, Cheesecake",
      "special": "White Chocolate Brownie"
    }
  ]
}
```

Start JSON Server
```
$ json-server --watch db.json
```

Open a browser window and go to http://localhost:3000/orders/1 to view the JSON result for the first order
```
{ "id": 1, "name": "Jane", "drink": "Americano w/ Creme","snack": "", "special": "Biscotti" }
```
**Good things to know:**
- It's best to place the db.json file in the root directory of the project.
- The db.json file is edited while you work on the application, so make sure to make a backup of your original data before beginning your prototype. 

## Routes
Here are the default routes to access the orders
```
GET     /orders
GET     /orders/{id}
POST    /orders
PUT     /orders 
DELETE  /orders/{id}
```






