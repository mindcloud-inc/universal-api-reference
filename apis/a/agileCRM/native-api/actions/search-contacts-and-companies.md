# Search Contacts and Companies with Agile CRM

Finds contacts and companies in Agile CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `/search`
- **Base URL:** `https://mindcloud.agilecrm.com/dev/api`
- **Official documentation:** [Search Contacts and Companies](https://github.com/agilecrm/rest-api#111-search-contactscompanies)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Search term (email, name, or keyword). |
| `type` | query | `string` | no | Entity type filter (PERSON or COMPANY). |
