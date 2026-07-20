# Get Company with SalesRender

Retrieves company details from SalesRender.

## Endpoint

- **Method:** `POST`
- **Path:** `:companyId/CRM`
- **Base URL:** `https://de.backend.salesrender.com/companies`
- **Official documentation:** [Get Company](https://wiki.salesrender.com/en/home/plugin/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | yes | GraphQL query document to send to the SalesRender CRM API. |
| `variables` | body | `object` | no | Optional GraphQL variables object. |
