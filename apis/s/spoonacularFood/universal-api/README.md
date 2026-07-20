# <img src="https://images.mindcloud.co/apps/icons/favicon-spoonacular-com-48x48_1777650522577.png" alt="Spoonacular Food logo" width="28" height="28"> Spoonacular Food: Universal API

Use Spoonacular's Recipe, Food, and Nutrition API to search recipes, ingredients, grocery products, menu items, nutrition data, wine pairings, and food classifiers.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/spoonacularFood/latest
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://spoonacular.com/food-api
- **Vendor API docs:** https://spoonacular.com/food-api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Recipes](actions/search-recipes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoonacularFood/latest/actions/search-recipes?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Food Image Classification

| Action | Method | Description |
| --- | --- | --- |
| [Classify Food Image by URL](actions/classify-food-image-by-url.md) | GET | Classifies a food image in Spoonacular Food by URL. |

### Food Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search All Food](actions/search-all-food.md) | GET | Finds food content in Spoonacular Food by keyword. |

### Grocery Product

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Products](actions/autocomplete-products.md) | GET | Finds product suggestions in Spoonacular Food by partial name. |
| [Get Product Information](actions/get-product-information.md) | GET | Retrieves grocery product information from Spoonacular Food. |
| [Search Grocery Product by UPC](actions/search-grocery-product-by-upc.md) | GET | Finds a grocery product in Spoonacular Food by UPC. |
| [Search Grocery Products](actions/search-grocery-products.md) | GET | Finds grocery products in Spoonacular Food by keyword. |

### Ingredient

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Ingredients](actions/autocomplete-ingredients.md) | GET | Finds ingredient suggestions in Spoonacular Food by partial name. |
| [Get Ingredient Information](actions/get-ingredient-information.md) | GET | Retrieves ingredient information from Spoonacular Food. |
| [Search Ingredients](actions/search-ingredients.md) | GET | Finds ingredients in Spoonacular Food by keyword. |

### Ingredient Conversion

| Action | Method | Description |
| --- | --- | --- |
| [Convert Ingredient Amount](actions/convert-ingredient-amount.md) | GET | Converts ingredient amounts in Spoonacular Food. |

### Ingredient Substitute

| Action | Method | Description |
| --- | --- | --- |
| [Get Ingredient Substitutes](actions/get-ingredient-substitutes.md) | GET | Retrieves ingredient substitutes from Spoonacular Food. |

### Menu Item

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Menu Items](actions/autocomplete-menu-items.md) | GET | Finds menu item suggestions in Spoonacular Food by partial name. |
| [Get Menu Item Information](actions/get-menu-item-information.md) | GET | Retrieves menu item information from Spoonacular Food. |
| [Search Menu Items](actions/search-menu-items.md) | GET | Finds menu items in Spoonacular Food by keyword. |

### Nutrition Answer

| Action | Method | Description |
| --- | --- | --- |
| [Quick Nutrition Answer](actions/quick-nutrition-answer.md) | GET | Retrieves a nutrition answer from Spoonacular Food. |

### Recipe

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Recipes](actions/autocomplete-recipes.md) | GET | Finds recipe suggestions in Spoonacular Food by partial title. |
| [Get Random Recipes](actions/get-random-recipes.md) | GET | Retrieves random recipes from Spoonacular Food. |
| [Get Recipe Information](actions/get-recipe-information.md) | GET | Retrieves recipe information from Spoonacular Food. |
| [Get Similar Recipes](actions/get-similar-recipes.md) | GET | Retrieves similar recipes from Spoonacular Food. |
| [Search Recipes](actions/search-recipes.md) | GET | Finds recipes in Spoonacular Food by keyword. |
| [Search Recipes by Ingredients](actions/search-recipes-by-ingredients.md) | GET | Finds recipes in Spoonacular Food by ingredient list. |
| [Search Recipes by Nutrients](actions/search-recipes-by-nutrients.md) | GET | Finds recipes in Spoonacular Food by nutrient limits. |

### Recipe Instruction

| Action | Method | Description |
| --- | --- | --- |
| [Get Analyzed Recipe Instructions](actions/get-analyzed-recipe-instructions.md) | GET | Retrieves analyzed recipe instructions from Spoonacular Food. |

### Recipe Nutrition

| Action | Method | Description |
| --- | --- | --- |
| [Get Recipe Nutrition](actions/get-recipe-nutrition.md) | GET | Retrieves recipe nutrition data from Spoonacular Food. |

### Recipe Query

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Recipe Search Query](actions/analyze-recipe-search-query.md) | GET | Retrieves parsed recipe query details from Spoonacular Food. |

### Recipe Summary

| Action | Method | Description |
| --- | --- | --- |
| [Summarize Recipe](actions/summarize-recipe.md) | GET | Retrieves a recipe summary from Spoonacular Food. |

### Wine Pairing

| Action | Method | Description |
| --- | --- | --- |
| [Get Wine Pairing](actions/get-wine-pairing.md) | GET | Retrieves wine pairings from Spoonacular Food for a dish. |

### Wine Recommendation

| Action | Method | Description |
| --- | --- | --- |
| [Get Wine Recommendation](actions/get-wine-recommendation.md) | GET | Retrieves wine recommendations from Spoonacular Food. |

