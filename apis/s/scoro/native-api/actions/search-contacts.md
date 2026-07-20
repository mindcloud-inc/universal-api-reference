# Search Contacts with Scoro

Finds contacts in Scoro.

## Endpoint

- **Method:** `POST`
- **Path:** `contacts`
- **Base URL:** `{subdomain}`
- **Official documentation:** [Search Contacts](https://api.scoro.com/api/v2#contactsApiV2Docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter.name` | body | `string` | no | Exact contact name filter. |
| `filter.is_client` | body | `boolean` | no | Filter contacts by client flag. |
| `filter.modified_date.start` | body | `date` | no | Start of modified date range. |
| `filter.modified_date.end` | body | `date` | no | End of modified date range. |
