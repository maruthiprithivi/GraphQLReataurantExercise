# GraphQLReataurantExercise

MITxPro GraphQL Restaurant Exercise

**Usage:** <br>
Clone the repo to your local machine and run `$> npm install` to install the node dependencies.

Then open this URL `localhost:5500` in your local machines webbrowser to access the GrapiQL interface and you can perform **CRUD** actions using the following queries.

```
# Get one restaurant by ID
query getRestaurant($iid: Int = 1) {
  restaurant(id: $iid) {
    id
    name
    description
    dishes {
      name
      price
    }
  }
}

# Get all restaurants
query getRestaurants {
  restaurants {
    id
    name
    description
    dishes {
      name
      price
    }
  }
}

# Add a new restaurant
mutation setRestaurant {
  setrestaurant(input: {
    id: 4,
    name: "Granite",
    description: "American",
  }) {
    name
    description
  }
}

# Edit an existing restaurants name by referenicing to their ID
mutation editRestaurant($idd: Int = 1, $name: String = "OLDO") {
  editrestaurant(id: $idd, name: $name) {
    name
    description
  }
}

# Delete a restautant using ID
mutation deleteRestaurant($iid: Int = 1) {
  deleterestaurant(id: $iid) {
    ok
  }
}
```
