# Autocomplete Menu Item Search with Spoonacular

Autocompletes menu items in Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/menuItems/suggest`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Autocomplete Menu Item Search](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Required by the Spoonacular endpoint. |
