# List Project Databases with Prisma Postgres

Retrieves project databases from Prisma Postgres.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{projectId}/databases`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [List Project Databases](https://api.prisma.io/v1/swagger-editor)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project identifier. |
| `cursor` | query | `string` | no | — |
| `limit` | query | `number` | no | — |
