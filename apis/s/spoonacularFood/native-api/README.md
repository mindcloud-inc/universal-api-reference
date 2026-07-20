# Spoonacular Food: Native API Reference

A consolidated summary of Spoonacular Food's API configuration and 28 documented operations, with links to official documentation.

- **Official docs:** https://spoonacular.com/food-api/docs
- **API base URL:** `https://api.spoonacular.com`

## Authentication

### API Key

Authenticate Spoonacular requests with an API key supplied as the case-sensitive apiKey query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://spoonacular.com/food-api/docs#Authentication)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (28 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Recipe Search Query](actions/analyze-recipe-search-query.md) | `GET /recipes/queries/analyze` | [docs](https://spoonacular.com/food-api/docs#Analyze-a-Recipe-Search-Query) |
| [Autocomplete Ingredients](actions/autocomplete-ingredients.md) | `GET /food/ingredients/autocomplete` | [docs](https://spoonacular.com/food-api/docs#Autocomplete-Ingredient-Search) |
| [Autocomplete Menu Items](actions/autocomplete-menu-items.md) | `GET /food/menuItems/suggest` | [docs](https://spoonacular.com/food-api/docs#Autocomplete-Menu-Item-Search) |
| [Autocomplete Products](actions/autocomplete-products.md) | `GET /food/products/suggest` | [docs](https://spoonacular.com/food-api/docs#Autocomplete-Product-Search) |
| [Autocomplete Recipes](actions/autocomplete-recipes.md) | `GET /recipes/autocomplete` | [docs](https://spoonacular.com/food-api/docs#Autocomplete-Recipe-Search) |
| [Classify Food Image by URL](actions/classify-food-image-by-url.md) | `GET /food/images/classify` | [docs](https://spoonacular.com/food-api/docs#Image-Classification-by-URL) |
| [Convert Ingredient Amount](actions/convert-ingredient-amount.md) | `GET /recipes/convert` | [docs](https://spoonacular.com/food-api/docs#Convert-Amounts) |
| [Get Analyzed Recipe Instructions](actions/get-analyzed-recipe-instructions.md) | `GET /recipes/:id/analyzedInstructions` | [docs](https://spoonacular.com/food-api/docs#Get-Analyzed-Recipe-Instructions) |
| [Get Ingredient Information](actions/get-ingredient-information.md) | `GET /food/ingredients/:id/information` | [docs](https://spoonacular.com/food-api/docs#Get-Ingredient-Information) |
| [Get Ingredient Substitutes](actions/get-ingredient-substitutes.md) | `GET /food/ingredients/substitutes` | [docs](https://spoonacular.com/food-api/docs#Get-Ingredient-Substitutes) |
| [Get Menu Item Information](actions/get-menu-item-information.md) | `GET /food/menuItems/:id` | [docs](https://spoonacular.com/food-api/docs#Get-Menu-Item-Information) |
| [Get Product Information](actions/get-product-information.md) | `GET /food/products/:id` | [docs](https://spoonacular.com/food-api/docs#Get-Product-Information) |
| [Get Random Recipes](actions/get-random-recipes.md) | `GET /recipes/random` | [docs](https://spoonacular.com/food-api/docs#Get-Random-Recipes) |
| [Get Recipe Information](actions/get-recipe-information.md) | `GET /recipes/:id/information` | [docs](https://spoonacular.com/food-api/docs#Get-Recipe-Information) |
| [Get Recipe Nutrition](actions/get-recipe-nutrition.md) | `GET /recipes/:id/nutritionWidget.json` | [docs](https://spoonacular.com/food-api/docs#Nutrition-by-ID) |
| [Get Similar Recipes](actions/get-similar-recipes.md) | `GET /recipes/:id/similar` | [docs](https://spoonacular.com/food-api/docs#Get-Similar-Recipes) |
| [Get Wine Pairing](actions/get-wine-pairing.md) | `GET /food/wine/pairing` | [docs](https://spoonacular.com/food-api/docs#Wine-Pairing) |
| [Get Wine Recommendation](actions/get-wine-recommendation.md) | `GET /food/wine/recommendation` | [docs](https://spoonacular.com/food-api/docs#Wine-Recommendation) |
| [Quick Nutrition Answer](actions/quick-nutrition-answer.md) | `GET /recipes/quickAnswer` | [docs](https://spoonacular.com/food-api/docs#Quick-Answer) |
| [Search All Food](actions/search-all-food.md) | `GET /food/search` | [docs](https://spoonacular.com/food-api/docs#Search-All-Food) |
| [Search Grocery Product by UPC](actions/search-grocery-product-by-upc.md) | `GET /food/products/upc/:upc` | [docs](https://spoonacular.com/food-api/docs#Search-Grocery-Products-by-UPC) |
| [Search Grocery Products](actions/search-grocery-products.md) | `GET /food/products/search` | [docs](https://spoonacular.com/food-api/docs#Search-Grocery-Products) |
| [Search Ingredients](actions/search-ingredients.md) | `GET /food/ingredients/search` | [docs](https://spoonacular.com/food-api/docs#Ingredient-Search) |
| [Search Menu Items](actions/search-menu-items.md) | `GET /food/menuItems/search` | [docs](https://spoonacular.com/food-api/docs#Search-Menu-Items) |
| [Search Recipes](actions/search-recipes.md) | `GET /recipes/complexSearch` | [docs](https://spoonacular.com/food-api/docs#Search-Recipes) |
| [Search Recipes by Ingredients](actions/search-recipes-by-ingredients.md) | `GET /recipes/findByIngredients` | [docs](https://spoonacular.com/food-api/docs#Search-Recipes-by-Ingredients) |
| [Search Recipes by Nutrients](actions/search-recipes-by-nutrients.md) | `GET /recipes/findByNutrients` | [docs](https://spoonacular.com/food-api/docs#Search-Recipes-by-Nutrients) |
| [Summarize Recipe](actions/summarize-recipe.md) | `GET /recipes/:id/summary` | [docs](https://spoonacular.com/food-api/docs#Summarize-Recipe) |
