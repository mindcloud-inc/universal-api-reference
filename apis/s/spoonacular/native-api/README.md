# Spoonacular: Native API Reference

A consolidated summary of Spoonacular's API configuration and 104 documented operations, with links to official documentation.

- **Official docs:** https://spoonacular.com/food-api/docs
- **API base URL:** `https://api.spoonacular.com`

## Authentication

### API Key

Use your Spoonacular API key. Runtime requests send the key as the provider-supported x-api-key header.

### Credentials

- **API Key:** `apiKey` · required · Your Spoonacular API key.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://spoonacular.com/food-api/docs)

## Endpoints (104 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Custom Foods](actions/add-custom-foods.md) | `POST /food/customFoods/add` | [docs](https://spoonacular.com/food-api/docs) |
| [Add Meal Plan Template](actions/add-meal-plan-template.md) | `POST /mealplanner/{username}/templates` | [docs](https://spoonacular.com/food-api/docs) |
| [Add to Meal Plan](actions/add-to-meal-plan.md) | `POST /mealplanner/{username}/items` | [docs](https://spoonacular.com/food-api/docs) |
| [Add to Shopping List](actions/add-to-shopping-list.md) | `POST /mealplanner/{username}/shopping-list/items` | [docs](https://spoonacular.com/food-api/docs) |
| [Analyze a Recipe Search Query](actions/analyze-a-recipe-search-query.md) | `GET /recipes/queries/analyze` | [docs](https://spoonacular.com/food-api/docs) |
| [Analyze Recipe](actions/analyze-recipe.md) | `POST /recipes/analyze` | [docs](https://spoonacular.com/food-api/docs) |
| [Analyze Recipe Instructions](actions/analyze-recipe-instructions.md) | `POST /recipes/analyzeInstructions` | [docs](https://spoonacular.com/food-api/docs) |
| [Autocomplete Ingredient Search](actions/autocomplete-ingredient-search.md) | `GET /food/ingredients/autocomplete` | [docs](https://spoonacular.com/food-api/docs) |
| [Autocomplete Menu Item Search](actions/autocomplete-menu-item-search.md) | `GET /food/menuItems/suggest` | [docs](https://spoonacular.com/food-api/docs) |
| [Autocomplete Product Search](actions/autocomplete-product-search.md) | `GET /food/products/suggest` | [docs](https://spoonacular.com/food-api/docs) |
| [Autocomplete Recipe Search](actions/autocomplete-recipe-search.md) | `GET /recipes/autocomplete` | [docs](https://spoonacular.com/food-api/docs) |
| [Classify Cuisine](actions/classify-cuisine.md) | `POST /recipes/cuisine` | [docs](https://spoonacular.com/food-api/docs) |
| [Classify Grocery Product](actions/classify-grocery-product.md) | `POST /food/products/classify` | [docs](https://spoonacular.com/food-api/docs) |
| [Classify Grocery Product Bulk](actions/classify-grocery-product-bulk.md) | `POST /food/products/classifyBatch` | [docs](https://spoonacular.com/food-api/docs) |
| [Clear Meal Plan Day](actions/clear-meal-plan-day.md) | `DELETE /mealplanner/{username}/day/{date}` | [docs](https://spoonacular.com/food-api/docs) |
| [Compute Glycemic Load](actions/compute-glycemic-load.md) | `POST /food/ingredients/glycemicLoad` | [docs](https://spoonacular.com/food-api/docs) |
| [Compute Ingredient Amount](actions/compute-ingredient-amount.md) | `GET /food/ingredients/{id}/amount` | [docs](https://spoonacular.com/food-api/docs) |
| [Compute Shopping List](actions/compute-shopping-list.md) | `POST /mealplanner/shopping-list/compute` | [docs](https://spoonacular.com/food-api/docs) |
| [Connect User](actions/connect-user.md) | `POST /users/connect` | [docs](https://spoonacular.com/food-api/docs) |
| [Conversation Suggests](actions/conversation-suggests.md) | `GET /food/converse/suggest` | [docs](https://spoonacular.com/food-api/docs) |
| [Convert Amounts](actions/convert-amounts.md) | `GET /recipes/convert` | [docs](https://spoonacular.com/food-api/docs) |
| [Create Recipe Card](actions/create-recipe-card.md) | `POST /recipes/visualizeRecipe` | [docs](https://spoonacular.com/food-api/docs) |
| [Delete from Meal Plan](actions/delete-from-meal-plan.md) | `DELETE /mealplanner/{username}/items/{id}` | [docs](https://spoonacular.com/food-api/docs) |
| [Delete from Shopping List](actions/delete-from-shopping-list.md) | `DELETE /mealplanner/{username}/shopping-list/items/{id}` | [docs](https://spoonacular.com/food-api/docs) |
| [Delete Meal Plan Template](actions/delete-meal-plan-template.md) | `DELETE /mealplanner/{username}/templates/{id}` | [docs](https://spoonacular.com/food-api/docs) |
| [Detect Food in Text](actions/detect-food-in-text.md) | `POST /food/detect` | [docs](https://spoonacular.com/food-api/docs) |
| [Dish Pairing for Wine](actions/dish-pairing-for-wine.md) | `GET /food/wine/dishes` | [docs](https://spoonacular.com/food-api/docs) |
| [Equipment by ID](actions/equipment-by-id.md) | `GET /recipes/{id}/equipmentWidget.json` | [docs](https://spoonacular.com/food-api/docs) |
| [Equipment by ID Image](actions/equipment-by-id-image.md) | `GET /recipes/{id}/equipmentWidget.png` | [docs](https://spoonacular.com/food-api/docs) |
| [Equipment by ID Widget](actions/equipment-by-id-widget.md) | `GET /recipes/{id}/equipmentWidget` | [docs](https://spoonacular.com/food-api/docs) |
| [Equipment Widget](actions/equipment-widget.md) | `POST /recipes/visualizeEquipment` | [docs](https://spoonacular.com/food-api/docs) |
| [Estimate Nutrients from Image](actions/estimate-nutrients-from-image.md) | `POST /recipes/estimateNutrients` | [docs](https://spoonacular.com/food-api/docs) |
| [Estimate Nutrition by Dish Name](actions/estimate-nutrition-by-dish-name.md) | `GET /recipes/guessNutrition` | [docs](https://spoonacular.com/food-api/docs) |
| [Extract Recipe from Website](actions/extract-recipe-from-website.md) | `GET /recipes/extract` | [docs](https://spoonacular.com/food-api/docs) |
| [Generate Meal Plan](actions/generate-meal-plan.md) | `GET /mealplanner/generate` | [docs](https://spoonacular.com/food-api/docs) |
| [Generate Shopping List](actions/generate-shopping-list.md) | `POST /mealplanner/{username}/shopping-list/{start-date}/{end-date}` | [docs](https://spoonacular.com/food-api/docs) |
| [Get Analyzed Recipe Instructions](actions/get-analyzed-recipe-instructions.md) | `GET /recipes/{id}/analyzedInstructions` | [docs](https://spoonacular.com/food-api/docs) |
| [Get Comparable Products](actions/get-comparable-products.md) | `GET /food/products/upc/{upc}/comparable` | [docs](https://spoonacular.com/food-api/docs) |
| [Get Ingredient Information](actions/get-ingredient-information.md) | `GET /food/ingredients/{id}/information` | [docs](https://spoonacular.com/food-api/docs) |
| [Get Ingredient Substitutes](actions/get-ingredient-substitutes.md) | `GET /food/ingredients/substitutes` | [docs](https://spoonacular.com/food-api/docs) |
| [Get Ingredient Substitutes by ID](actions/get-ingredient-substitutes-by-id.md) | `GET /food/ingredients/{id}/substitutes` | [docs](https://spoonacular.com/food-api/docs) |
| [Get Meal Plan Day](actions/get-meal-plan-day.md) | `GET /mealplanner/{username}/day/{date}` | [docs](https://spoonacular.com/food-api/docs) |
| [Get Meal Plan Template](actions/get-meal-plan-template.md) | `GET /mealplanner/{username}/templates/{id}` | [docs](https://spoonacular.com/food-api/docs) |
| [Get Meal Plan Templates](actions/get-meal-plan-templates.md) | `GET /mealplanner/{username}/templates` | [docs](https://spoonacular.com/food-api/docs) |
| [Get Meal Plan Week](actions/get-meal-plan-week.md) | `GET /mealplanner/{username}/week/{start-date}` | [docs](https://spoonacular.com/food-api/docs) |
| [Get Menu Item Information](actions/get-menu-item-information.md) | `GET /food/menuItems/{id}` | [docs](https://spoonacular.com/food-api/docs) |
| [Get Product Information](actions/get-product-information.md) | `GET /food/products/{id}` | [docs](https://spoonacular.com/food-api/docs) |
| [Get Random Recipes](actions/get-random-recipes.md) | `GET /recipes/random` | [docs](https://spoonacular.com/food-api/docs) |
| [Get Recipe Information](actions/get-recipe-information.md) | `GET /recipes/{id}/information` | [docs](https://spoonacular.com/food-api/docs) |
| [Get Recipe Information Bulk](actions/get-recipe-information-bulk.md) | `GET /recipes/informationBulk` | [docs](https://spoonacular.com/food-api/docs) |
| [Get Shopping List](actions/get-shopping-list.md) | `GET /mealplanner/{username}/shopping-list` | [docs](https://spoonacular.com/food-api/docs) |
| [Get Similar Recipes](actions/get-similar-recipes.md) | `GET /recipes/{id}/similar` | [docs](https://spoonacular.com/food-api/docs) |
| [Image Analysis by File](actions/image-analysis-by-file.md) | `POST /food/images/analyze` | [docs](https://spoonacular.com/food-api/docs) |
| [Image Analysis by URL](actions/image-analysis-by-url.md) | `GET /food/images/analyze` | [docs](https://spoonacular.com/food-api/docs) |
| [Image Classification by File](actions/image-classification-by-file.md) | `POST /food/images/classify` | [docs](https://spoonacular.com/food-api/docs) |
| [Image Classification by URL](actions/image-classification-by-url.md) | `GET /food/images/classify` | [docs](https://spoonacular.com/food-api/docs) |
| [Ingredient Search](actions/ingredient-search.md) | `GET /food/ingredients/search` | [docs](https://spoonacular.com/food-api/docs) |
| [Ingredients by ID](actions/ingredients-by-id.md) | `GET /recipes/{id}/ingredientWidget.json` | [docs](https://spoonacular.com/food-api/docs) |
| [Ingredients by ID Image](actions/ingredients-by-id-image.md) | `GET /recipes/{id}/ingredientWidget.png` | [docs](https://spoonacular.com/food-api/docs) |
| [Ingredients by ID Widget](actions/ingredients-by-id-widget.md) | `GET /recipes/{id}/ingredientWidget` | [docs](https://spoonacular.com/food-api/docs) |
| [Ingredients Widget](actions/ingredients-widget.md) | `POST /recipes/visualizeIngredients` | [docs](https://spoonacular.com/food-api/docs) |
| [Map Ingredients to Grocery Products](actions/map-ingredients-to-grocery-products.md) | `POST /food/ingredients/map` | [docs](https://spoonacular.com/food-api/docs) |
| [Menu Item Nutrition by ID Image](actions/menu-item-nutrition-by-id-image.md) | `GET /food/menuItems/{id}/nutritionWidget.png` | [docs](https://spoonacular.com/food-api/docs) |
| [Menu Item Nutrition by ID Widget](actions/menu-item-nutrition-by-id-widget.md) | `GET /food/menuItems/{id}/nutritionWidget` | [docs](https://spoonacular.com/food-api/docs) |
| [Menu Item Nutrition Label Image](actions/menu-item-nutrition-label-image.md) | `GET /food/menuItems/{id}/nutritionLabel.png` | [docs](https://spoonacular.com/food-api/docs) |
| [Menu Item Nutrition Label Widget](actions/menu-item-nutrition-label-widget.md) | `GET /food/menuItems/{id}/nutritionLabel` | [docs](https://spoonacular.com/food-api/docs) |
| [Nutrition by ID](actions/nutrition-by-id.md) | `GET /recipes/{id}/nutritionWidget.json` | [docs](https://spoonacular.com/food-api/docs) |
| [Parse Ingredients](actions/parse-ingredients.md) | `POST /recipes/parseIngredients` | [docs](https://spoonacular.com/food-api/docs) |
| [Price Breakdown by ID](actions/price-breakdown-by-id.md) | `GET /recipes/{id}/priceBreakdownWidget.json` | [docs](https://spoonacular.com/food-api/docs) |
| [Price Breakdown by ID Image](actions/price-breakdown-by-id-image.md) | `GET /recipes/{id}/priceBreakdownWidget.png` | [docs](https://spoonacular.com/food-api/docs) |
| [Price Breakdown by ID Widget](actions/price-breakdown-by-id-widget.md) | `GET /recipes/{id}/priceBreakdownWidget` | [docs](https://spoonacular.com/food-api/docs) |
| [Price Breakdown Widget](actions/price-breakdown-widget.md) | `POST /recipes/visualizePriceEstimator` | [docs](https://spoonacular.com/food-api/docs) |
| [Product Nutrition by ID Image](actions/product-nutrition-by-id-image.md) | `GET /food/products/{id}/nutritionWidget.png` | [docs](https://spoonacular.com/food-api/docs) |
| [Product Nutrition by ID Widget](actions/product-nutrition-by-id-widget.md) | `GET /food/products/{id}/nutritionWidget` | [docs](https://spoonacular.com/food-api/docs) |
| [Product Nutrition Label Image](actions/product-nutrition-label-image.md) | `GET /food/products/{id}/nutritionLabel.png` | [docs](https://spoonacular.com/food-api/docs) |
| [Product Nutrition Label Widget](actions/product-nutrition-label-widget.md) | `GET /food/products/{id}/nutritionLabel` | [docs](https://spoonacular.com/food-api/docs) |
| [Quick Answer](actions/quick-answer.md) | `GET /recipes/quickAnswer` | [docs](https://spoonacular.com/food-api/docs) |
| [Random Food Joke](actions/random-food-joke.md) | `GET /food/jokes/random` | [docs](https://spoonacular.com/food-api/docs) |
| [Random Food Trivia](actions/random-food-trivia.md) | `GET /food/trivia/random` | [docs](https://spoonacular.com/food-api/docs) |
| [Recipe Nutrition by ID Image](actions/recipe-nutrition-by-id-image.md) | `GET /recipes/{id}/nutritionWidget.png` | [docs](https://spoonacular.com/food-api/docs) |
| [Recipe Nutrition by ID Widget](actions/recipe-nutrition-by-id-widget.md) | `GET /recipes/{id}/nutritionWidget` | [docs](https://spoonacular.com/food-api/docs) |
| [Recipe Nutrition Label Image](actions/recipe-nutrition-label-image.md) | `GET /recipes/{id}/nutritionLabel.png` | [docs](https://spoonacular.com/food-api/docs) |
| [Recipe Nutrition Label Widget](actions/recipe-nutrition-label-widget.md) | `GET /recipes/{id}/nutritionLabel` | [docs](https://spoonacular.com/food-api/docs) |
| [Recipe Nutrition Widget](actions/recipe-nutrition-widget.md) | `POST /recipes/visualizeNutrition` | [docs](https://spoonacular.com/food-api/docs) |
| [Recipe Taste by ID Image](actions/recipe-taste-by-id-image.md) | `GET /recipes/{id}/tasteWidget.png` | [docs](https://spoonacular.com/food-api/docs) |
| [Recipe Taste by ID Widget](actions/recipe-taste-by-id-widget.md) | `GET /recipes/{id}/tasteWidget` | [docs](https://spoonacular.com/food-api/docs) |
| [Recipe Taste Widget](actions/recipe-taste-widget.md) | `POST /recipes/visualizeTaste` | [docs](https://spoonacular.com/food-api/docs) |
| [Search All Food](actions/search-all-food.md) | `GET /food/search` | [docs](https://spoonacular.com/food-api/docs) |
| [Search Custom Foods](actions/search-custom-foods.md) | `GET /food/customFoods/search` | [docs](https://spoonacular.com/food-api/docs) |
| [Search Food Videos](actions/search-food-videos.md) | `GET /food/videos/search` | [docs](https://spoonacular.com/food-api/docs) |
| [Search Grocery Products](actions/search-grocery-products.md) | `GET /food/products/search` | [docs](https://spoonacular.com/food-api/docs) |
| [Search Grocery Products by UPC](actions/search-grocery-products-by-upc.md) | `GET /food/products/upc/{upc}` | [docs](https://spoonacular.com/food-api/docs) |
| [Search Menu Items](actions/search-menu-items.md) | `GET /food/menuItems/search` | [docs](https://spoonacular.com/food-api/docs) |
| [Search Recipes](actions/search-recipes.md) | `GET /recipes/complexSearch` | [docs](https://spoonacular.com/food-api/docs) |
| [Search Recipes by Ingredients](actions/search-recipes-by-ingredients.md) | `GET /recipes/findByIngredients` | [docs](https://spoonacular.com/food-api/docs) |
| [Search Recipes by Nutrients](actions/search-recipes-by-nutrients.md) | `GET /recipes/findByNutrients` | [docs](https://spoonacular.com/food-api/docs) |
| [Search Restaurants](actions/search-restaurants.md) | `GET /food/restaurants/search` | [docs](https://spoonacular.com/food-api/docs) |
| [Search Site Content](actions/search-site-content.md) | `GET /food/site/search` | [docs](https://spoonacular.com/food-api/docs) |
| [Summarize Recipe](actions/summarize-recipe.md) | `GET /recipes/{id}/summary` | [docs](https://spoonacular.com/food-api/docs) |
| [Talk to Chatbot](actions/talk-to-chatbot.md) | `GET /food/converse` | [docs](https://spoonacular.com/food-api/docs) |
| [Taste by ID](actions/taste-by-id.md) | `GET /recipes/{id}/tasteWidget.json` | [docs](https://spoonacular.com/food-api/docs) |
| [Wine Description](actions/wine-description.md) | `GET /food/wine/description` | [docs](https://spoonacular.com/food-api/docs) |
| [Wine Pairing](actions/wine-pairing.md) | `GET /food/wine/pairing` | [docs](https://spoonacular.com/food-api/docs) |
| [Wine Recommendation](actions/wine-recommendation.md) | `GET /food/wine/recommendation` | [docs](https://spoonacular.com/food-api/docs) |
