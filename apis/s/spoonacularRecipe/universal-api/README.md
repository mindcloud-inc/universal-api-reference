# <img src="https://images.mindcloud.co/apps/icons/favicon-spoonacular-com-48x48-1_1777908693463.png" alt="Spoonacular Recipe logo" width="28" height="28"> Spoonacular Recipe: Universal API

Search, inspect, analyze, and enrich recipes using Spoonacular's Recipe, Food, and Nutrition API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/spoonacularRecipe/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://spoonacular.com/food-api
- **Vendor API docs:** https://spoonacular.com/food-api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Recipes](actions/search-recipes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularRecipe/latest/actions/search-recipes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Amount Conversion

| Action | Method | Description |
| --- | --- | --- |
| [Convert Recipe Amounts](actions/convert-recipe-amounts.md) | GET | Converts ingredient amounts between units in Spoonacular. |

### Cuisine Classification

| Action | Method | Description |
| --- | --- | --- |
| [Classify Cuisine](actions/classify-cuisine.md) | GET | Classifies a recipe's cuisine in Spoonacular. |

### Ingredient

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Ingredient Search](actions/autocomplete-ingredient-search.md) | GET | Finds ingredient name completions in Spoonacular. |
| [Get Ingredient Information](actions/get-ingredient-information.md) | GET | Retrieves detailed ingredient information from Spoonacular. |
| [Ingredient Search](actions/ingredient-search.md) | GET | Finds whole-food ingredients in Spoonacular. |

### Ingredient Amount

| Action | Method | Description |
| --- | --- | --- |
| [Compute Ingredient Amount](actions/compute-ingredient-amount.md) | GET | Computes ingredient amounts for nutrition goals in Spoonacular. |

### Ingredient Substitute

| Action | Method | Description |
| --- | --- | --- |
| [Get Ingredient Substitutes](actions/get-ingredient-substitutes.md) | GET | Finds ingredient substitutes in Spoonacular by name. |
| [Get Ingredient Substitutes by ID](actions/get-ingredient-substitutes-by-id.md) | GET | Finds ingredient substitutes in Spoonacular by ID. |

### Parsed Ingredient

| Action | Method | Description |
| --- | --- | --- |
| [Parse Ingredients](actions/parse-ingredients.md) | GET | Parses ingredients from plain text in Spoonacular. |

### Recipe

| Action | Method | Description |
| --- | --- | --- |
| [Extract Recipe from Website](actions/extract-recipe-from-website.md) | GET | Extracts recipe data from a website in Spoonacular. |
| [Get Random Recipes](actions/get-random-recipes.md) | GET | Retrieves random recipe results from Spoonacular. |
| [Get Recipe Information](actions/get-recipe-information.md) | GET | Retrieves detailed recipe information from Spoonacular. |
| [Get Recipe Information Bulk](actions/get-recipe-information-bulk.md) | GET | Retrieves information for multiple recipes from Spoonacular. |
| [Get Similar Recipes](actions/get-similar-recipes.md) | GET | Retrieves recipes similar to a Spoonacular recipe. |
| [Search Recipes](actions/search-recipes.md) | GET | Finds recipes in Spoonacular with advanced filters. |
| [Search Recipes by Ingredients](actions/search-recipes-by-ingredients.md) | GET | Finds recipes in Spoonacular by ingredients. |
| [Search Recipes by Nutrients](actions/search-recipes-by-nutrients.md) | GET | Finds recipes in Spoonacular by nutrient constraints. |

### Recipe Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Recipe](actions/analyze-recipe.md) | GET | Analyzes raw recipe data in Spoonacular. |

### Recipe Card

| Action | Method | Description |
| --- | --- | --- |
| [Create Recipe Card](actions/create-recipe-card.md) | GET | Generates a recipe card from a Spoonacular recipe. |

### Recipe Instructions

| Action | Method | Description |
| --- | --- | --- |
| [Get Analyzed Recipe Instructions](actions/get-analyzed-recipe-instructions.md) | GET | Retrieves analyzed instructions for a Spoonacular recipe. |

### Recipe Instructions Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Recipe Instructions](actions/analyze-recipe-instructions.md) | GET | Analyzes recipe instructions in Spoonacular. |

### Recipe Query Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Recipe Search Query](actions/analyze-recipe-search-query.md) | GET | Analyzes a recipe search query in Spoonacular. |

### Recipe Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Recipe Search](actions/autocomplete-recipe-search.md) | GET | Finds recipe name completions in Spoonacular. |

### Recipe Summary

| Action | Method | Description |
| --- | --- | --- |
| [Summarize Recipe](actions/summarize-recipe.md) | GET | Retrieves a recipe summary from Spoonacular. |

