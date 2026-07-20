# Search Company Contacts with PBX Yeastar

Finds company contacts in PBX Yeastar by search criteria.

## Endpoint

- **Method:** `GET`
- **Path:** `/company_contact/search`
- **Base URL:** `{baseUrl}/openapi/v1.0`
- **Official documentation:** [Search Company Contacts](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/search-specific-company-contacts.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_value` | query | `string` | no | Search keyword for filtering company contacts. |
