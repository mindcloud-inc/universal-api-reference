# Search Icons with Freepik

Finds Freepik icons by search term and filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/icons`
- **Base URL:** `https://api.freepik.com`
- **Official documentation:** [Search Icons](https://docs.freepik.com/api-reference/icons/get-all-icons-by-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `term` | query | `string` | no | Icon search term. |
| `per_page` | query | `number` | no | Number of icons to return per page. |
| `page` | query | `number` | no | One-based icons page to request. |
