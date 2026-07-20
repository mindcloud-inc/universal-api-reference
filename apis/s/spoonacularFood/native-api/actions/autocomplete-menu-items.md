# Autocomplete Menu Items with Spoonacular Food

Finds menu item suggestions in Spoonacular Food by partial name.

## Endpoint

- **Method:** `GET`
- **Path:** `/food/menuItems/suggest`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Autocomplete Menu Items](https://spoonacular.com/food-api/docs#Autocomplete-Menu-Item-Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Menu item name prefix to autocomplete. |
