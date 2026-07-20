# List Roles V2 with Sumo Logic

Retrieves roles from your Sumo Logic organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/roles`
- **Base URL:** `https://api.sumologic.com/api`
- **Official documentation:** [List Roles V2](https://api.sumologic.com/docs/#/roleManagementV2/listRolesV2)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Only return roles matching the given name. |
