# List Endpoints with Svix

Retrieves endpoints from Svix.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/app/{app_id}/endpoint`
- **Base URL:** `https://api.us.svix.com`
- **Official documentation:** [List Endpoints](https://api.svix.com/docs#operation/v1.endpoint.list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_id` | path | `string` | yes | The application's ID or UID. |
| `iterator` | query | `string` | no | The iterator returned from a prior invocation. |
| `limit` | query | `number` | no | Limit the number of returned items. |
| `order` | query | `string` | no | The sorting order of the returned items. |
