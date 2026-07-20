# Revoke Permission with KleverKey

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/organizations/:organizationId/permissions/:lockId/:userId`
- **Base URL:** `https://api.kleverkey.com`
- **Official documentation:** [Revoke Permission](https://portal.kleverkey.com/documentation/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `organizationId` | path | `number` | yes |
| `lockId` | path | `number` | yes |
| `userId` | path | `number` | yes |
