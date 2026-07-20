# List Widgets with Common Ninja

Retrieves user widgets from Common Ninja.

## Endpoint

- **Method:** `GET`
- **Path:** `/widgets`
- **Base URL:** `https://api.commoninja.com/platform/api/v1`
- **Official documentation:** [List Widgets](https://developers.commoninja.com/docs/api/widgets/widgets-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Comma-separated list of fields to include in the response. |
| `limit` | query | `number` | no | Maximum number of widgets to return. |
| `projectId` | query | `string` | no | Filter widgets by project ID. |
| `query` | query | `string` | no | Filter widgets by search query. |
| `type` | query | `string` | no | Filter widgets by widget type. |
