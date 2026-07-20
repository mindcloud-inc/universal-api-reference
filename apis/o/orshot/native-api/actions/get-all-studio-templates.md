# Get All Studio Templates with Orshot

## Endpoint

- **Method:** `GET`
- **Path:** `/studio/templates/all`
- **Base URL:** `https://api.orshot.com/v1`
- **Official documentation:** [Get All Studio Templates](https://orshot.com/docs/api-reference/studio-templates-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `embedId` | query | `string` | no | Embed instance ID for user-specific filtering. Must be used together with Embed User ID. |
| `embedUserId` | query | `string` | no | User ID for template filtering. Must be used together with Embed ID. |
