# Create Project with Prisma Postgres

Creates a new project in Prisma Postgres.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [Create Project](https://api.prisma.io/v1/swagger-editor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createDatabase` | body | `boolean` | no | Whether Prisma should create a default database with the new project. |
| `name` | body | `string` | no | Display name for the new project. |
| `region` | body | `list` | no | Project region. |
