# List Guides with Dubble

Retrieves a list of guides from Dubble.

## Endpoint

- **Method:** `GET`
- **Path:** `/guides`
- **Base URL:** `https://api.dubble.so/v1`
- **Official documentation:** [List Guides](https://dubble.readme.io/reference/getguides)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collection` | query | `string` | no | Filter guides by collection ID |
| `created_after` | query | `string` | no | Filter guides created after a date |
| `cursor` | query | `string` | no | Cursor returned from the previous page |
| `per_page` | query | `number` | no | Number of items per page |
| `search` | query | `string` | no | Search guides by title |
| `sort` | query | `string` | no | Sort direction: asc or desc |
| `updated_after` | query | `string` | no | Filter guides updated after a date |
