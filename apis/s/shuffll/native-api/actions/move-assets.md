# Move Assets with Shuffll

Updates asset locations in Shuffll.

## Endpoint

- **Method:** `PUT`
- **Path:** `/auth/organization/:organizationId/workspace/:workspaceId/assets/move`
- **Base URL:** `https://api.shuffll.com/api/v1`
- **Official documentation:** [Move Assets](https://api-docs.shuffll.com/apis/assets/moveassets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assetIds[]` | body | `array<string>` | yes | Asset ids to move. |
| `organizationId` | path | `string` | yes | Shuffll organization id. |
| `toFolder` | body | `string` | yes | Destination folder name. |
| `workspaceId` | path | `string` | yes | Shuffll workspace id. |
