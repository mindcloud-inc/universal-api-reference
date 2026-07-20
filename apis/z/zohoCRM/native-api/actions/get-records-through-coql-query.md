# Get Records through COQL Query with Zoho CRM

Retrieves records from Zoho CRM using a COQL query.

## Endpoint

- **Method:** `POST`
- **Path:** `/coql`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Get Records through COQL Query](https://www.zoho.com/crm/developer/docs/api/v8/Get-Records-through-COQL-Query.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `select_query` | body | `string` | yes | Single read-only COQL SELECT query. Use one SELECT statement only. |
