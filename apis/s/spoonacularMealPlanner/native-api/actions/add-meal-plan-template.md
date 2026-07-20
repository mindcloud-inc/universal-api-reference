# Add Meal Plan Template with Spoonacular Meal Planner

Creates a meal plan template in Spoonacular Meal Planner.

## Endpoint

- **Method:** `POST`
- **Path:** `/mealplanner/{username}/templates`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Add Meal Plan Template](https://spoonacular.com/food-api/docs#Add-Meal-Plan-Template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hash` | query | `string` | no | Private hash returned by Connect User. |
| `items` | body | `string` | no | Meal plan template items array. |
| `name` | body | `string` | no | Meal plan template name. |
| `publishAsPublic` | body | `string` | no | Whether to publish the template publicly. |
| `username` | path | `string` | no | Spoonacular username returned by Connect User. |
