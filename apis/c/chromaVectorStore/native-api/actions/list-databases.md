# List Databases with Chroma Vector Store

Retrieves tenant database records from Chroma.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/tenants/:tenant/databases`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [List Databases](https://docs.trychroma.com/reference/chroma-api/database/list-databases)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `limit` | query | `string` | no |
| `offset` | query | `string` | no |
| `tenant` | path | `string` | no |
