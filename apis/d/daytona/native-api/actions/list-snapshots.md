# List Snapshots with Daytona

Retrieves all snapshots from Daytona.

## Endpoint

- **Method:** `GET`
- **Path:** `/snapshots`
- **Base URL:** `https://app.daytona.io/api`
- **Official documentation:** [List Snapshots](https://www.daytona.io/docs/tools/api/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter by partial snapshot name match. |
