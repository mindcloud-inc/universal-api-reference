# Create Article Category with Everbill

Creates a new article category in Everbill.

## Endpoint

- **Method:** `POST`
- **Path:** `/article_categories/add`
- **Base URL:** `https://api.everbill.eu`
- **Official documentation:** [Create Article Category](https://api.swaggerhub.com/apis/everbill1/everbill/1.10/swagger.json#/paths/~1article_categories~1add/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | name request body field. |
| `color` | body | `string` | no | color request body field. |
| `favorit` | body | `boolean` | no | favorit request body field. |
| `parent_id` | body | `number` | no | parent_id request body field. |
