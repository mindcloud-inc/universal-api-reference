# Add to Shopping List with Spoonacular Meal Planner

Creates a shopping list item in Spoonacular Meal Planner.

## Endpoint

- **Method:** `POST`
- **Path:** `/mealplanner/{username}/shopping-list/items`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Add to Shopping List](https://spoonacular.com/food-api/docs#Add-to-Shopping-List)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `aisle` | body | `string` | no | Optional aisle for the item. |
| `hash` | query | `string` | no | Private hash returned by Connect User. |
| `item` | body | `string` | no | Shopping list item text, such as 1 package baking powder. |
| `parse` | body | `string` | no | Whether to parse the food item; set false for non-food items. |
| `username` | path | `string` | no | Spoonacular username returned by Connect User. |
