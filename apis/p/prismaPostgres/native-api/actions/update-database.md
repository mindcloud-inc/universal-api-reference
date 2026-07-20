# Update Database with Prisma Postgres

Updates an existing database in Prisma Postgres.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/databases/{databaseId}`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [Update Database](https://api.prisma.io/v1/swagger-editor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database identifier to update. |
| `name` | body | `string` | no | New display name for the database. |
