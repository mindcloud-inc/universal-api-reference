# Grant Permission with KleverKey

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/organizations/:organizationId/permissions/:lockId/:userId`
- **Base URL:** `https://api.kleverkey.com`
- **Official documentation:** [Grant Permission](https://portal.kleverkey.com/documentation/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `number` | yes | — |
| `lockId` | path | `number` | yes | — |
| `userId` | path | `number` | yes | — |
| `permissionType` | body | `number` | yes | 1 = Always, 2 = TimeProfile |
