# Update Access Group Partially with KleverKey

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/organizations/:organizationId/access-groups/:accessGroupId`
- **Base URL:** `https://api.kleverkey.com`
- **Official documentation:** [Update Access Group Partially](https://portal.kleverkey.com/documentation/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | — |
| `accessGroupId` | path | `number` | yes | — |
| `op` | body | `string` | yes | JSON Patch operation. Use replace for /userIds or /lockIds updates. |
| `path` | body | `string` | yes | JSON Patch target path. Supported values from docs are /userIds and /lockIds. |
| `value[]` | body | `array<number>` | no | Replacement IDs for the target path. |
