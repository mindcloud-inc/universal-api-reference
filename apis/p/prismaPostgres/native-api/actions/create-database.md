# Create Database with Prisma Postgres

Creates a new database in Prisma Postgres.

## Endpoint

- **Method:** `POST`
- **Path:** `/databases`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [Create Database](https://api.prisma.io/v1/swagger-editor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isDefault` | body | `boolean` | no | Whether the created database should become the project default. |
| `name` | body | `string` | no | Display name for the new database. |
| `projectId` | body | `string` | yes | Project that will own the new database. |
| `region` | body | `list` | no | Target region for the database. Use inherit to follow the project default. |
| `source` | body | `object` | no | Optional source object to create the database from. |
