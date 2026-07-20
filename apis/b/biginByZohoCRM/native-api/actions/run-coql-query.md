# Run COQL Query with Bigin by Zoho CRM

Runs a COQL query in Bigin by Zoho CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/coql`
- **Base URL:** `{api_domain}/bigin/v2`
- **Official documentation:** [Run COQL Query](https://www.bigin.com/developer/docs/apis/v2/get-records-using-coql-query.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `select_query` | body | `string` | yes | The COQL query string to execute. |
