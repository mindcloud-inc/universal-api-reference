# Update Group with FileCloud

Replaces an existing group in FileCloud.

## Endpoint

- **Method:** `PUT`
- **Path:** `/scim/Groups/:id`
- **Base URL:** `https://mindcloud.filecloudtrial.com/api/v1`
- **Official documentation:** [Update Group](https://fcapi-v1.filecloud.com/#/scim/updateScimGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Group ID. |
| `displayName` | body | `string` | yes | Group display name. |
| `members[]` | body | `array<object>` | no | Group member objects, for example [{"value":"69ce3ad60c4bfb47f20ff372"}]. |
