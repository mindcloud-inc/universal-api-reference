# List Connections with Prisma Postgres

Retrieves connections from Prisma Postgres.

## Endpoint

- **Method:** `GET`
- **Path:** `/connections`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [List Connections](https://api.prisma.io/v1/swagger-editor)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | query | `string` | no | Optional database to filter returned connections by. |
| `cursor` | query | `string` | no | — |
| `limit` | query | `number` | no | — |
