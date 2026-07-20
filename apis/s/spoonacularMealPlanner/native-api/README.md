# Spoonacular Meal Planner: Native API Reference

A consolidated summary of Spoonacular Meal Planner's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://spoonacular.com/food-api/docs
- **API base URL:** `https://api.spoonacular.com`

## Authentication

### Spoonacular API Key

Authenticate requests with a Spoonacular API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://spoonacular.com/food-api/docs#Authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `number` in the query string to set the page size (default 1; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Meal Plan Template](actions/add-meal-plan-template.md) | `POST /mealplanner/{username}/templates` | [docs](https://spoonacular.com/food-api/docs#Add-Meal-Plan-Template) |
| [Add to Meal Plan](actions/add-to-meal-plan.md) | `POST /mealplanner/{username}/items` | [docs](https://spoonacular.com/food-api/docs#Add-to-Meal-Plan) |
| [Add to Shopping List](actions/add-to-shopping-list.md) | `POST /mealplanner/{username}/shopping-list/items` | [docs](https://spoonacular.com/food-api/docs#Add-to-Shopping-List) |
| [Autocomplete Recipe Search](actions/autocomplete-recipe-search.md) | `GET /recipes/autocomplete` | [docs](https://spoonacular.com/food-api/docs#Autocomplete-Recipe-Search) |
| [Clear Meal Plan Day](actions/clear-meal-plan-day.md) | `DELETE /mealplanner/{username}/day/{date}` | [docs](https://spoonacular.com/food-api/docs#Clear-Meal-Plan-Day) |
| [Compute Shopping List](actions/compute-shopping-list.md) | `POST /mealplanner/shopping-list/compute` | [docs](https://spoonacular.com/food-api/docs#Compute-Shopping-List) |
| [Connect User](actions/connect-user.md) | `POST /users/connect` | [docs](https://spoonacular.com/food-api/docs#Connect-User) |
| [Delete from Meal Plan](actions/delete-from-meal-plan.md) | `DELETE /mealplanner/{username}/items/{id}` | [docs](https://spoonacular.com/food-api/docs#Delete-from-Meal-Plan) |
| [Delete from Shopping List](actions/delete-from-shopping-list.md) | `DELETE /mealplanner/{username}/shopping-list/items/{id}` | [docs](https://spoonacular.com/food-api/docs#Delete-from-Shopping-List) |
| [Delete Meal Plan Template](actions/delete-meal-plan-template.md) | `DELETE /mealplanner/{username}/templates/{id}` | [docs](https://spoonacular.com/food-api/docs#Delete-Meal-Plan-Template) |
| [Generate Meal Plan](actions/generate-meal-plan.md) | `GET /mealplanner/generate` | [docs](https://spoonacular.com/food-api/docs#Generate-Meal-Plan) |
| [Generate Shopping List](actions/generate-shopping-list.md) | `POST /mealplanner/{username}/shopping-list/{start-date}/{end-date}` | [docs](https://spoonacular.com/food-api/docs#Generate-Shopping-List) |
| [Get Analyzed Recipe Instructions](actions/get-analyzed-recipe-instructions.md) | `GET /recipes/{id}/analyzedInstructions` | [docs](https://spoonacular.com/food-api/docs#Get-Analyzed-Recipe-Instructions) |
| [Get Meal Plan Day](actions/get-meal-plan-day.md) | `GET /mealplanner/{username}/day/{date}` | [docs](https://spoonacular.com/food-api/docs#Get-Meal-Plan-Day) |
| [Get Meal Plan Template](actions/get-meal-plan-template.md) | `GET /mealplanner/{username}/templates/{id}` | [docs](https://spoonacular.com/food-api/docs#Get-Meal-Plan-Template) |
| [Get Meal Plan Templates](actions/get-meal-plan-templates.md) | `GET /mealplanner/{username}/templates` | [docs](https://spoonacular.com/food-api/docs#Get-Meal-Plan-Templates) |
| [Get Meal Plan Week](actions/get-meal-plan-week.md) | `GET /mealplanner/{username}/week/{start-date}` | [docs](https://spoonacular.com/food-api/docs#Get-Meal-Plan-Week) |
| [Get Random Recipes](actions/get-random-recipes.md) | `GET /recipes/random` | [docs](https://spoonacular.com/food-api/docs#Get-Random-Recipes) |
| [Get Recipe Information](actions/get-recipe-information.md) | `GET /recipes/{id}/information` | [docs](https://spoonacular.com/food-api/docs#Get-Recipe-Information) |
| [Get Shopping List](actions/get-shopping-list.md) | `GET /mealplanner/{username}/shopping-list` | [docs](https://spoonacular.com/food-api/docs#Get-Shopping-List) |
| [Get Similar Recipes](actions/get-similar-recipes.md) | `GET /recipes/{id}/similar` | [docs](https://spoonacular.com/food-api/docs#Get-Similar-Recipes) |
| [Search Recipes](actions/search-recipes.md) | `GET /recipes/complexSearch` | [docs](https://spoonacular.com/food-api/docs#Search-Recipes) |
| [Search Recipes by Ingredients](actions/search-recipes-by-ingredients.md) | `GET /recipes/findByIngredients` | [docs](https://spoonacular.com/food-api/docs#Search-Recipes-by-Ingredients) |
| [Search Recipes by Nutrients](actions/search-recipes-by-nutrients.md) | `GET /recipes/findByNutrients` | [docs](https://spoonacular.com/food-api/docs#Search-Recipes-by-Nutrients) |
