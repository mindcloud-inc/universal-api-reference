# Create Connection with Prisma Postgres

Creates a new connection in Prisma Postgres.

## Endpoint

- **Method:** `POST`
- **Path:** `/connections`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [Create Connection](https://api.prisma.io/v1/swagger-editor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | body | `string` | yes | Database that will own the new connection. |
| `name` | body | `string` | yes | Display name for the new connection. |
