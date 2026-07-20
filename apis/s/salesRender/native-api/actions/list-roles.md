# List Roles with SalesRender

Retrieves roles from SalesRender.

## Endpoint

- **Method:** `POST`
- **Path:** `:companyId/CRM`
- **Base URL:** `https://de.backend.salesrender.com/companies`
- **Official documentation:** [List Roles](https://wiki.salesrender.com/en/home/plugin/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | GraphQL query to execute. |
| `variables` | body | `object` | no | GraphQL variables object. |
