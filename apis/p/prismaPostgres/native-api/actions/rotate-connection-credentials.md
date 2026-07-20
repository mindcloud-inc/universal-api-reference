# Rotate Connection Credentials with Prisma Postgres

Rotates credentials for a Prisma Postgres connection.

## Endpoint

- **Method:** `POST`
- **Path:** `/connections/{id}/rotate`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [Rotate Connection Credentials](https://api.prisma.io/v1/swagger-editor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Connection identifier to rotate. |
