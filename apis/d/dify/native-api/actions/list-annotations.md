# List Annotations with Dify

Retrieves annotations from Dify.

## Endpoint

- **Method:** `GET`
- **Path:** `/apps/annotations`
- **Base URL:** `https://api.dify.ai/v1`
- **Official documentation:** [List Annotations](https://docs.dify.ai/api-reference/annotations/list-annotations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number to return. |
| `keyword` | query | `string` | no | Keyword filter for annotations. |
