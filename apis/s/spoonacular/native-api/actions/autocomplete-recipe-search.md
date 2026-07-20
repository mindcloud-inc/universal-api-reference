# Autocomplete Recipe Search with Spoonacular

Autocompletes recipe names in Spoonacular.

## Endpoint

- **Method:** `GET`
- **Path:** `/recipes/autocomplete`
- **Base URL:** `https://api.spoonacular.com`
- **Official documentation:** [Autocomplete Recipe Search](https://spoonacular.com/food-api/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Required by the Spoonacular endpoint. |
