# List Jobs with SqlBak

Retrieves jobs from SqlBak.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs`
- **Base URL:** `https://sqlbak.com/public-api/v1`
- **Official documentation:** [List Jobs](https://sqlbak.docs.apiary.io/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter jobs whose name contains this substring. |
| `job_type` | query | `list` | no | Filter jobs by job type. Accepted values: `backup`, `maintenance`. |
| `server_id` | query | `number` | no | Filter jobs by server ID. |
| `dbms_connection_id` | query | `number` | no | Filter jobs by DBMS connection ID. |
