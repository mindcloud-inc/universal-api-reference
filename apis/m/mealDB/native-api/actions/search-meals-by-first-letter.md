# Search Meals by First Letter with MealDB

## Endpoint

- **Method:** `GET`
- **Path:** `/search.php`
- **Base URL:** `https://www.themealdb.com/api/json/v1/{apiKey}`
- **Official documentation:** [Search Meals by First Letter](https://www.themealdb.com/api.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `f` | query | `string` | yes | Single letter used to search meal names. Maximum length: 1. |
