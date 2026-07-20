# Query Records with Vtiger CRM

Finds records in Vtiger CRM by query string.

## Endpoint

- **Method:** `GET`
- **Path:** `/query`
- **Base URL:** `{apiBaseUrl}`
- **Official documentation:** [Query Records](https://vtap.vtiger.com/platform/rest-apis.html#query)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Vtiger query string, for example select id, firstname, lastname from Contacts limit 0, 2; |
