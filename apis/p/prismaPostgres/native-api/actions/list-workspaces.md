# List Workspaces with Prisma Postgres

Retrieves workspaces from Prisma Postgres.

## Endpoint

- **Method:** `GET`
- **Path:** `/workspaces`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [List Workspaces](https://api.prisma.io/v1/swagger-editor)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cursor` | query | `string` | no |
| `limit` | query | `number` | no |
