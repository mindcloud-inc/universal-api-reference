# List Databases with Prisma Postgres

Retrieves databases from Prisma Postgres.

## Endpoint

- **Method:** `GET`
- **Path:** `/databases`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [List Databases](https://api.prisma.io/v1/swagger-editor)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | query | `string` | no | Optional project to filter returned databases by. |
| `cursor` | query | `string` | no | — |
| `limit` | query | `number` | no | — |
