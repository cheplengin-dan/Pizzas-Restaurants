# Pizza API

This is a Rails API backend for managing restaurants and pizzas. It provides CRUD operations for restaurants, pizzas, and restaurant-pizza associations.

## API Endpoints

The API provides the following endpoints:

- GET /restaurants: Retrieve all restaurants.
- GET /restaurants/:id: Retrieve a specific restaurant by ID.
- DELETE /restaurants/:id: Delete a restaurant by ID.
- GET /pizzas: Retrieve all pizzas.
- POST /restaurant_pizzas: Create a new restaurant-pizza association.

## Models

The API includes the following models:

- Restaurant: Represents a restaurant with attributes such as name and address.
- Pizza: Represents a pizza with attributes such as name and ingredients.
- RestaurantPizza: Represents the association between a restaurant and a pizza, including the price.

The models have the following relationships:

- A Restaurant has many Pizzas through RestaurantPizza.
- A Pizza has many Restaurants through RestaurantPizza.
- A RestaurantPizza belongs to a Restaurant and belongs to a Pizza.

## Validations

The RestaurantPizza model has a validation for the price attribute, which must be between 1 and 30.
