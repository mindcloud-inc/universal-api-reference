# List Roles with Sumo Logic

Retrieves roles from your Sumo Logic organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/roles`
- **Base URL:** `https://api.sumologic.com/api`
- **Official documentation:** [List Roles](https://api.sumologic.com/docs/#/roleManagement/listRoles)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Only return roles matching the given name. |
