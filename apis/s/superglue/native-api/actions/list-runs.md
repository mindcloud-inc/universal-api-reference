# List Runs with Superglue

Retrieves runs from Superglue.

## Endpoint

- **Method:** `GET`
- **Path:** `/runs`
- **Base URL:** `https://api.superglue.ai/v1`
- **Official documentation:** [List Runs](https://docs.superglue.cloud/api-reference/runs/list-runs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `toolId` | query | `string` | no | Filter runs by tool ID. |
| `status` | query | `list` | no | Filter runs by status. Accepted values: `aborted`, `failed`, `running`, `success`. |
| `requestSources` | query | `string` | no | Filter by comma-separated request sources. |
| `userId` | query | `string` | no | Filter runs by user ID. |
| `systemId` | query | `string` | no | Filter runs by system ID. |
