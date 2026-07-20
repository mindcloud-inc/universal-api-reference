# Search Categories by Path with Ecwid

Finds categories in Ecwid by path.

## Endpoint

- **Method:** `GET`
- **Path:** `/:storeId/categoriesByPath`
- **Base URL:** `https://app.ecwid.com/api/v3`
- **Official documentation:** [Search Categories by Path](https://docs.ecwid.com/api-reference/rest-api/categories/search-categories-by-path)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `path` | query | `string` | yes | Category path to resolve. |
| `delimeter` | query | `string` | yes | Path segment delimiter. |
