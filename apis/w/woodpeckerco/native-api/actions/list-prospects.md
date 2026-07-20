# List Prospects with Woodpecker.co

Retrieves prospects from the Woodpecker database.

## Endpoint

- **Method:** `GET`
- **Path:** `/rest/v1/prospects`
- **Base URL:** `https://api.woodpecker.co`
- **Official documentation:** [List Prospects](https://developers.woodpecker.co/docs/prospects/get-prospects/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number. |
| `per_page` | query | `number` | no | Number of prospects per page. |
| `sort` | query | `string` | no | Woodpecker sort expression. |
