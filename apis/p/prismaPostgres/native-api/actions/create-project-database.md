# Create Project Database with Prisma Postgres

Creates a new project database in Prisma Postgres.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/{projectId}/databases`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [Create Project Database](https://api.prisma.io/v1/swagger-editor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Project that will own the new database. |
| `name` | body | `string` | no | Display name for the project database. |
| `region` | body | `list` | no | Target region for the new project database. |
| `isDefault` | body | `boolean` | no | Whether the project database should become default. |
| `fromDatabase` | body | `object` | no | — |
| `source` | body | `object` | no | Optional source object to create the project database from. |
