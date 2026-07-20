# List Agents with Zaia

Retrieves agents from your Zaia workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/agents`
- **Base URL:** `https://api.endless.zaia.app`
- **Official documentation:** [List Agents](https://docs.zaia.app/documentation/api-reference-alpha/reference/agents)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search term to filter agents by name, internal name, role, or prompt. |
| `squadId` | query | `string` | no | Optional squad UUID used to list agents in a specific squad. |
| `versionId` | query | `string` | no | Optional version UUID used to list agents for a specific version. |
