# List Database Connections with Prisma Postgres

Retrieves database connections from Prisma Postgres.

## Endpoint

- **Method:** `GET`
- **Path:** `/databases/{databaseId}/connections`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [List Database Connections](https://api.prisma.io/v1/swagger-editor)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database identifier. |
| `cursor` | query | `string` | no | — |
| `limit` | query | `number` | no | — |
