# List Email List Records with Toofr

Retrieves email list records from a Toofr list.

## Endpoint

- **Method:** `GET`
- **Path:** `/lists/:list_id/list_records`
- **Base URL:** `https://www.findemails.com/api/v1`
- **Official documentation:** [List Email List Records](https://developer.findemails.com/?from=explinks.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | Email list ID. |
| `page` | query | `number` | no | Optional provider page number. |
