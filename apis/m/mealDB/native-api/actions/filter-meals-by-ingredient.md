# Filter Meals by Ingredient with MealDB

## Endpoint

- **Method:** `GET`
- **Path:** `/filter.php`
- **Base URL:** `https://www.themealdb.com/api/json/v1/{apiKey}`
- **Official documentation:** [Filter Meals by Ingredient](https://www.themealdb.com/api.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `i` | query | `string` | yes | Ingredient name; spaces are represented with underscores by the provider. |
