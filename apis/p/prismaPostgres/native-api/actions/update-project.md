# Update Project with Prisma Postgres

Updates an existing project in Prisma Postgres.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/{id}`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [Update Project](https://api.prisma.io/v1/swagger-editor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Project identifier to update. |
| `name` | body | `string` | no | New display name for the project. |
| `settings` | body | `object` | no | Project settings object. |
