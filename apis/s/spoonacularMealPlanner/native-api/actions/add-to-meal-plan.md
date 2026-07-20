# Add to Meal Plan with Spoonacular Meal Planner

Creates a meal plan item in Spoonacular Meal Planner.

## Endpoint

- **Method:** `POST`
- **Path:** `/mealplanner/{username}/items`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Add to Meal Plan](https://spoonacular.com/food-api/docs#Add-to-Meal-Plan)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | body | `string` | no | Meal plan date in yyyy-mm-dd format. |
| `hash` | query | `string` | no | Private hash returned by Connect User. |
| `position` | body | `string` | no | Position in the meal slot. |
| `slot` | body | `string` | no | Meal slot: 1 breakfast, 2 lunch, or 3 dinner. |
| `type` | body | `string` | no | Meal plan item type, such as RECIPE, PRODUCT, MENU_ITEM, CUSTOM_FOOD, or INGREDIENTS. |
| `username` | path | `string` | no | Spoonacular username returned by Connect User. |
| `value` | body | `string` | no | Meal plan item value object for the selected type. |
