# Update User with SalesRender

Updates an existing user in SalesRender.

## Endpoint

- **Method:** `POST`
- **Path:** `:companyId/CRM`
- **Base URL:** `https://de.backend.salesrender.com/companies`
- **Official documentation:** [Update User](https://wiki.salesrender.com/en/home/plugin/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | GraphQL mutation to execute. |
| `variables` | body | `object` | no | GraphQL variables object. Set `input` to a valid UpdateUserInput payload. |
