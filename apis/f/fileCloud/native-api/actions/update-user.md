# Update User with FileCloud

Replaces an existing user in FileCloud.

## Endpoint

- **Method:** `PUT`
- **Path:** `/scim/Users/:id`
- **Base URL:** `https://mindcloud.filecloudtrial.com/api/v1`
- **Official documentation:** [Update User](https://fcapi-v1.filecloud.com/#/scim/updateScimUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | User ID. |
| `userName` | body | `string` | yes | User login name. |
| `displayName` | body | `string` | yes | Name that appears on the user interface. |
| `emails[]` | body | `array<object>` | no | Email objects, for example [{"value":"apps@mindcloud.co","type":"work","primary":true}]. |
| `active` | body | `boolean` | no | Whether the user is active. |
