# List Integrations with Prisma Postgres

Retrieves integrations from Prisma Postgres.

## Endpoint

- **Method:** `GET`
- **Path:** `/integrations`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [List Integrations](https://api.prisma.io/v1/swagger-editor)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | query | `string` | yes | Workspace whose integrations should be listed. |
| `cursor` | query | `string` | no | — |
| `limit` | query | `number` | no | — |
