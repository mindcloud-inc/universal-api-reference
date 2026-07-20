# Autocomplete Search with AdvantShop

Finds product and category matches in AdvantShop.

## Endpoint

- **Method:** `POST`
- **Path:** `/search/autocomplete`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Autocomplete Search](https://www.advantshop.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | Text to autocomplete against products and categories. |
