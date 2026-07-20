# Create Database with Chroma Vector Store

Creates a new database in Chroma.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tenants/:tenant/databases`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Create Database](https://docs.trychroma.com/reference/chroma-api/database/create-database)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `tenant` | path | `string` | yes |
