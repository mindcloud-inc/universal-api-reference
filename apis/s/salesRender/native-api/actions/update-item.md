# Update Item with SalesRender

Updates an existing item in SalesRender.

## Endpoint

- **Method:** `POST`
- **Path:** `:companyId/CRM`
- **Base URL:** `https://de.backend.salesrender.com/companies`
- **Official documentation:** [Update Item](https://wiki.salesrender.com/en/home/plugin/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | GraphQL mutation to execute. |
| `variables` | body | `object` | no | GraphQL variables object. Set `input` to a valid UpdateItemInput payload. |
