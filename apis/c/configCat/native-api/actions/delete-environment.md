# Delete Environment with ConfigCat

Deletes an existing environment from ConfigCat.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/environments/:environmentId`
- **Base URL:** `https://api.configcat.com`
- **Official documentation:** [Delete Environment](https://configcat.com/docs/api/reference/delete-environment/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentId` | path | `string` | yes | The identifier of the Environment. |
| `cleanupAuditLogs` | query | `boolean` | no | Whether related audit logs should also be cleaned up. |
