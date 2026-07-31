# <img src="https://images.mindcloud.co/apps/icons/mealdb_1785426405168.png" alt="MealDB logo" width="28" height="28"> MealDB: Universal API

MealDB through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mealDB/latest
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Filter Meals by Area](actions/filter-meals-by-area.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mealDB/latest/actions/filter-meals-by-area?connectionId=$CONNECTION_ID&area=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Area

| Action | Method | Description |
| --- | --- | --- |
| [List Meal Areas](actions/list-meal-areas.md) | GET |  |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Meal Categories](actions/list-meal-categories.md) | GET |  |

### Ingredient

| Action | Method | Description |
| --- | --- | --- |
| [List Meal Ingredients](actions/list-meal-ingredients.md) | GET |  |

### Meal

| Action | Method | Description |
| --- | --- | --- |
| [Filter Meals by Area](actions/filter-meals-by-area.md) | GET |  |
| [Filter Meals by Category](actions/filter-meals-by-category.md) | GET |  |
| [Filter Meals by Ingredient](actions/filter-meals-by-ingredient.md) | GET |  |
| [Get Meal by ID](actions/get-meal-by-id.md) | GET |  |
| [Get Random Meal](actions/get-random-meal.md) | GET |  |
| [Search Meals by First Letter](actions/search-meals-by-first-letter.md) | GET |  |
| [Search Meals by Name](actions/search-meals-by-name.md) | GET |  |

