# List Workspace Integrations with Prisma Postgres

Retrieves workspace integrations from Prisma Postgres.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces/{workspaceId}/integrations`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [List Workspace Integrations](https://api.prisma.io/v1/swagger-editor)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Workspace identifier. |
| `cursor` | query | `string` | no | — |
| `limit` | query | `number` | no | — |
