# List Cocktails by First Letter with CocktailDB

## Endpoint

- **Method:** `GET`
- **Path:** `/search.php`
- **Base URL:** `https://www.thecocktaildb.com/api/json/v1/{apiKey}`
- **Official documentation:** [List Cocktails by First Letter](https://www.thecocktaildb.com/api.php)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `f` | query | `string` | yes | Return cocktails whose names start with this letter. |
