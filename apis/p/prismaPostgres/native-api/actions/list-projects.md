# List Projects with Prisma Postgres

Retrieves projects from Prisma Postgres.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [List Projects](https://api.prisma.io/v1/swagger-editor)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cursor` | query | `string` | no |
| `limit` | query | `number` | no |
