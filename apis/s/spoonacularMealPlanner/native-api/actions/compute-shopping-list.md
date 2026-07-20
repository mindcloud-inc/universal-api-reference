# Compute Shopping List with Spoonacular Meal Planner

Computes a shopping list from food strings in Spoonacular Meal Planner.

## Endpoint

- **Method:** `POST`
- **Path:** `/mealplanner/shopping-list/compute`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Compute Shopping List](https://spoonacular.com/food-api/docs#Compute-Shopping-List)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `items[]` | body | `array<string>` | yes | Array of simple food strings to compute into a shopping list. |
