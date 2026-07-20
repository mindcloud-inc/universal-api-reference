# Delete Assets with Shuffll

Deletes existing assets from Shuffll.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/auth/organization/:organizationId/workspace/:workspaceId/assets`
- **Base URL:** `https://api.shuffll.com/api/v1`
- **Official documentation:** [Delete Assets](https://api-docs.shuffll.com/apis/assets/deleteassets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assetIds[]` | body | `array<string>` | yes | Asset ids to delete. |
| `organizationId` | path | `string` | yes | Shuffll organization id. |
| `workspaceId` | path | `string` | yes | Shuffll workspace id. |
