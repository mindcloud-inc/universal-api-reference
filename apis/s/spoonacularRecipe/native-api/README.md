# Spoonacular Recipe: Native API Reference

A consolidated summary of Spoonacular Recipe's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://spoonacular.com/food-api/docs
- **API base URL:** `https://api.spoonacular.com`

## Authentication

### API Key

Authenticate Spoonacular Food API requests with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://spoonacular.com/food-api/docs#Authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `number` in the query string to set the page size (default 5; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `eq`.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Recipe](actions/analyze-recipe.md) | `POST /recipes/analyze` | [docs](https://spoonacular.com/food-api/docs#Analyze-Recipe) |
| [Analyze Recipe Instructions](actions/analyze-recipe-instructions.md) | `POST /recipes/analyzeInstructions` | [docs](https://spoonacular.com/food-api/docs#Analyze-Recipe-Instructions) |
| [Analyze Recipe Search Query](actions/analyze-recipe-search-query.md) | `GET /recipes/queries/analyze` | [docs](https://spoonacular.com/food-api/docs#Analyze-a-Recipe-Search-Query) |
| [Autocomplete Ingredient Search](actions/autocomplete-ingredient-search.md) | `GET /food/ingredients/autocomplete` | [docs](https://spoonacular.com/food-api/docs#Autocomplete-Ingredient-Search) |
| [Autocomplete Recipe Search](actions/autocomplete-recipe-search.md) | `GET /recipes/autocomplete` | [docs](https://spoonacular.com/food-api/docs#Autocomplete-Recipe-Search) |
| [Classify Cuisine](actions/classify-cuisine.md) | `POST /recipes/cuisine` | [docs](https://spoonacular.com/food-api/docs#Classify-Cuisine) |
| [Compute Ingredient Amount](actions/compute-ingredient-amount.md) | `GET /food/ingredients/{id}/amount` | [docs](https://spoonacular.com/food-api/docs#Compute-Ingredient-Amount) |
| [Convert Recipe Amounts](actions/convert-recipe-amounts.md) | `GET /recipes/convert` | [docs](https://spoonacular.com/food-api/docs#Convert-Amounts) |
| [Create Recipe Card](actions/create-recipe-card.md) | `GET /recipes/{id}/card` | [docs](https://spoonacular.com/food-api/docs#Create-Recipe-Card) |
| [Extract Recipe from Website](actions/extract-recipe-from-website.md) | `GET /recipes/extract` | [docs](https://spoonacular.com/food-api/docs#Extract-Recipe-from-Website) |
| [Get Analyzed Recipe Instructions](actions/get-analyzed-recipe-instructions.md) | `GET /recipes/{id}/analyzedInstructions` | [docs](https://spoonacular.com/food-api/docs#Get-Analyzed-Recipe-Instructions) |
| [Get Ingredient Information](actions/get-ingredient-information.md) | `GET /food/ingredients/{id}/information` | [docs](https://spoonacular.com/food-api/docs#Get-Ingredient-Information) |
| [Get Ingredient Substitutes](actions/get-ingredient-substitutes.md) | `GET /food/ingredients/substitutes` | [docs](https://spoonacular.com/food-api/docs#Get-Ingredient-Substitutes) |
| [Get Ingredient Substitutes by ID](actions/get-ingredient-substitutes-by-id.md) | `GET /food/ingredients/{id}/substitutes` | [docs](https://spoonacular.com/food-api/docs#Get-Ingredient-Substitutes-by-ID) |
| [Get Random Recipes](actions/get-random-recipes.md) | `GET /recipes/random` | [docs](https://spoonacular.com/food-api/docs#Get-Random-Recipes) |
| [Get Recipe Information](actions/get-recipe-information.md) | `GET /recipes/{id}/information` | [docs](https://spoonacular.com/food-api/docs#Get-Recipe-Information) |
| [Get Recipe Information Bulk](actions/get-recipe-information-bulk.md) | `GET /recipes/informationBulk` | [docs](https://spoonacular.com/food-api/docs#Get-Recipe-Information-Bulk) |
| [Get Similar Recipes](actions/get-similar-recipes.md) | `GET /recipes/{id}/similar` | [docs](https://spoonacular.com/food-api/docs#Get-Similar-Recipes) |
| [Ingredient Search](actions/ingredient-search.md) | `GET /food/ingredients/search` | [docs](https://spoonacular.com/food-api/docs#Ingredient-Search) |
| [Parse Ingredients](actions/parse-ingredients.md) | `POST /recipes/parseIngredients` | [docs](https://spoonacular.com/food-api/docs#Parse-Ingredients) |
| [Search Recipes](actions/search-recipes.md) | `GET /recipes/complexSearch` | [docs](https://spoonacular.com/food-api/docs#Search-Recipes-Complex) |
| [Search Recipes by Ingredients](actions/search-recipes-by-ingredients.md) | `GET /recipes/findByIngredients` | [docs](https://spoonacular.com/food-api/docs#Search-Recipes-by-Ingredients) |
| [Search Recipes by Nutrients](actions/search-recipes-by-nutrients.md) | `GET /recipes/findByNutrients` | [docs](https://spoonacular.com/food-api/docs#Search-Recipes-by-Nutrients) |
| [Summarize Recipe](actions/summarize-recipe.md) | `GET /recipes/{id}/summary` | [docs](https://spoonacular.com/food-api/docs#Summarize-Recipe) |
