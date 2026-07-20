# List Database Backups with Prisma Postgres

Retrieves database backups from Prisma Postgres.

## Endpoint

- **Method:** `GET`
- **Path:** `/databases/{databaseId}/backups`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [List Database Backups](https://api.prisma.io/v1/swagger-editor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database identifier. |
| `limit` | query | `number` | no | — |
