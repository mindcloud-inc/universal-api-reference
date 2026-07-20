# List Latest Notifications with Pushpad

Retrieves the latest notifications from a Pushpad project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/notifications`
- **Base URL:** `https://pushpad.xyz/api/v1`
- **Official documentation:** [List Latest Notifications](https://pushpad.xyz/docs/rest_api#notifications_api_docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `page` | query | `number` | no |
| `project_id` | path | `number` | yes |
