# Create database with Chroma Cloud

Creates a database in Chroma Cloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/tenants/:tenant/databases`
- **Base URL:** `https://api.trychroma.com`
- **Official documentation:** [Create database](https://docs.trychroma.com/reference/chroma-api/database/create-database)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
