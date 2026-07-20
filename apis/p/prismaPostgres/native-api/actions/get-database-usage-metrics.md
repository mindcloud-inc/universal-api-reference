# Get Database Usage Metrics with Prisma Postgres

Retrieves database usage metrics from Prisma Postgres.

## Endpoint

- **Method:** `GET`
- **Path:** `/databases/{databaseId}/usage`
- **Base URL:** `https://api.prisma.io/v1`
- **Official documentation:** [Get Database Usage Metrics](https://api.prisma.io/v1/swagger-editor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `databaseId` | path | `string` | yes | Database identifier. |
| `endDate` | query | `date` | no | End of the usage window. |
| `startDate` | query | `date` | no | Start of the usage window. |
