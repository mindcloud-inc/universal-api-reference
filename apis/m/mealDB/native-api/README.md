# MealDB: Native API Reference

A consolidated summary of MealDB's API configuration and 10 documented operations.

- **API base URL:** `https://www.themealdb.com/api/json/v1/{apiKey}`

## Authentication

### API key

TheMealDB API key used as the versioned URL path segment.

### Credentials

- **TheMealDB API key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.themealdb.com/api.php)

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Filter Meals by Area](actions/filter-meals-by-area.md) | `GET /filter.php` | [docs](https://www.themealdb.com/api.php) |
| [Filter Meals by Category](actions/filter-meals-by-category.md) | `GET /filter.php` | [docs](https://www.themealdb.com/api.php) |
| [Filter Meals by Ingredient](actions/filter-meals-by-ingredient.md) | `GET /filter.php` | [docs](https://www.themealdb.com/api.php) |
| [Get Meal by ID](actions/get-meal-by-id.md) | `GET /lookup.php` | [docs](https://www.themealdb.com/api.php) |
| [Get Random Meal](actions/get-random-meal.md) | `GET /random.php` | [docs](https://www.themealdb.com/api.php) |
| [List Meal Areas](actions/list-meal-areas.md) | `GET /list.php?a=list` | [docs](https://www.themealdb.com/api.php) |
| [List Meal Categories](actions/list-meal-categories.md) | `GET /categories.php` | [docs](https://www.themealdb.com/api.php) |
| [List Meal Ingredients](actions/list-meal-ingredients.md) | `GET /list.php?i=list` | [docs](https://www.themealdb.com/api.php) |
| [Search Meals by First Letter](actions/search-meals-by-first-letter.md) | `GET /search.php` | [docs](https://www.themealdb.com/api.php) |
| [Search Meals by Name](actions/search-meals-by-name.md) | `GET /search.php` | [docs](https://www.themealdb.com/api.php) |
