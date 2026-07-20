# Patch User with FileCloud

Partially updates an existing user in FileCloud.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/scim/Users/:id`
- **Base URL:** `https://mindcloud.filecloudtrial.com/api/v1`
- **Official documentation:** [Patch User](https://fcapi-v1.filecloud.com/#/scim/patchScimUser)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | User ID. |
| `Operations[]` | body | `array<object>` | yes | Patch operations, for example [{"op":"replace","path":"displayName","value":"apps"}]. |
