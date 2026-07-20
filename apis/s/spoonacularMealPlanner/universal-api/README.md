# <img src="https://images.mindcloud.co/apps/icons/favicon-spoonacular-com-48x48-1_1777908657410.png" alt="Spoonacular Meal Planner logo" width="28" height="28"> Spoonacular Meal Planner: Universal API

Plan meals and discover recipe options with Spoonacular's Recipe, Food, and Nutrition API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/spoonacularMealPlanner/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://spoonacular.com/food-api
- **Vendor API docs:** https://spoonacular.com/food-api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Recipes by Ingredients](actions/search-recipes-by-ingredients.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularMealPlanner/latest/actions/search-recipes-by-ingredients?connectionId=$CONNECTION_ID&ingredients=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Meal Plan

| Action | Method | Description |
| --- | --- | --- |
| [Generate Meal Plan](actions/generate-meal-plan.md) | GET | Retrieves a generated meal plan from Spoonacular Meal Planner. |
| [Get Meal Plan Day](actions/get-meal-plan-day.md) | GET | Retrieves a daily meal plan from Spoonacular Meal Planner. |
| [Get Meal Plan Week](actions/get-meal-plan-week.md) | GET | Retrieves a weekly meal plan from Spoonacular Meal Planner. |

### Meal Plan Day

| Action | Method | Description |
| --- | --- | --- |
| [Clear Meal Plan Day](actions/clear-meal-plan-day.md) | DELETE | Deletes all meal plan items for a day from Spoonacular Meal Planner. |

### Meal Plan Item

| Action | Method | Description |
| --- | --- | --- |
| [Add to Meal Plan](actions/add-to-meal-plan.md) | POST | Creates a meal plan item in Spoonacular Meal Planner. |
| [Delete from Meal Plan](actions/delete-from-meal-plan.md) | DELETE | Deletes a meal plan item from Spoonacular Meal Planner. |

### Meal Plan Template

| Action | Method | Description |
| --- | --- | --- |
| [Add Meal Plan Template](actions/add-meal-plan-template.md) | POST | Creates a meal plan template in Spoonacular Meal Planner. |
| [Delete Meal Plan Template](actions/delete-meal-plan-template.md) | DELETE | Deletes a meal plan template from Spoonacular Meal Planner. |
| [Get Meal Plan Template](actions/get-meal-plan-template.md) | GET | Retrieves a meal plan template from Spoonacular Meal Planner. |
| [Get Meal Plan Templates](actions/get-meal-plan-templates.md) | GET | Retrieves meal plan templates from Spoonacular Meal Planner. |

### Recipe

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Recipe Search](actions/autocomplete-recipe-search.md) | GET | Finds recipe suggestions in Spoonacular Meal Planner by title prefix. |
| [Get Random Recipes](actions/get-random-recipes.md) | GET | Retrieves random recipes from Spoonacular Meal Planner. |
| [Get Recipe Information](actions/get-recipe-information.md) | GET | Retrieves recipe details from Spoonacular Meal Planner. |
| [Get Similar Recipes](actions/get-similar-recipes.md) | GET | Retrieves similar recipes from Spoonacular Meal Planner. |
| [Search Recipes](actions/search-recipes.md) | GET | Finds recipes in Spoonacular Meal Planner by search criteria. |
| [Search Recipes by Ingredients](actions/search-recipes-by-ingredients.md) | GET | Finds recipes in Spoonacular Meal Planner by ingredients. |
| [Search Recipes by Nutrients](actions/search-recipes-by-nutrients.md) | GET | Finds recipes in Spoonacular Meal Planner by nutrient ranges. |

### Recipe Instructions

| Action | Method | Description |
| --- | --- | --- |
| [Get Analyzed Recipe Instructions](actions/get-analyzed-recipe-instructions.md) | GET | Retrieves analyzed recipe instructions from Spoonacular Meal Planner. |

### Shopping List

| Action | Method | Description |
| --- | --- | --- |
| [Compute Shopping List](actions/compute-shopping-list.md) | POST | Computes a shopping list from food strings in Spoonacular Meal Planner. |
| [Generate Shopping List](actions/generate-shopping-list.md) | POST | Creates a shopping list from a meal plan in Spoonacular Meal Planner. |
| [Get Shopping List](actions/get-shopping-list.md) | GET | Retrieves a shopping list from Spoonacular Meal Planner. |

### Shopping List Item

| Action | Method | Description |
| --- | --- | --- |
| [Add to Shopping List](actions/add-to-shopping-list.md) | POST | Creates a shopping list item in Spoonacular Meal Planner. |
| [Delete from Shopping List](actions/delete-from-shopping-list.md) | DELETE | Deletes a shopping list item from Spoonacular Meal Planner. |

### Spoonacular User

| Action | Method | Description |
| --- | --- | --- |
| [Connect User](actions/connect-user.md) | POST | Creates a connected user in Spoonacular Meal Planner. |

