# Get Filter with Google Mail

Retrieves a filter from Gmail settings.

## Endpoint

- **Method:** `GET`
- **Path:** `/settings/filters/:id`
- **Base URL:** `https://gmail.googleapis.com/gmail/v1/users/:userId`
- **Official documentation:** [Get Filter](https://developers.google.com/workspace/gmail/api/reference/rest/v1/users.settings.filters/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Filter ID to fetch. |
