# Create Database Connection String with Prisma Postgres

Creates a database connection string in Prisma Postgres.

## Endpoint

- **Method:** `POST`
- **Path:** `/databases/{databaseId}/connections`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [Create Database Connection String](https://api.prisma.io/v1/swagger-editor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database identifier. |
| `name` | body | `string` | yes | Display name for the generated connection string. |
