# Delete Key with Lokalise

Deletes an existing key from Lokalise.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/projects/:project_id/keys/:key_id`
- **Base URL:** `https://api.lokalise.com/api2`
- **Official documentation:** [Delete Key](https://developers.lokalise.com/reference/delete-a-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key_id` | path | `string` | no | Lokalise key identifier. |
| `project_id` | path | `string` | no | Lokalise project identifier. |
