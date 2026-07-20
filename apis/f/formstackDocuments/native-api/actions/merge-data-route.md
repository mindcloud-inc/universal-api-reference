# Merge Data Route with Formstack Documents

Merges data through a data route in Formstack Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `https://www.webmerge.me/route/:id/:key`
- **Base URL:** `https://www.webmerge.me/api`
- **Official documentation:** [Merge Data Route](https://www.webmerge.me/developers/routes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `download` | query | `string` | no | Return merged file contents when set to 1 |
| `id` | path | `string` | yes | ID of the data route to merge |
| `key` | path | `string` | yes | Merge key from the data route URL |
| `test` | query | `string` | no | Use test mode when set to 1 |
