# List Document Fields with Formstack Documents

Retrieves document fields from Formstack Documents.

## Endpoint

- **Method:** `GET`
- **Path:** `/documents/:id/fields`
- **Base URL:** `https://www.webmerge.me/api`
- **Official documentation:** [List Document Fields](https://www.webmerge.me/developers/documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attributes` | query | `string` | no | Include full field attributes when set to 1 |
| `id` | path | `string` | yes | The document ID. |
