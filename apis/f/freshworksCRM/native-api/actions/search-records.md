# Search Records with Freshworks CRM

Finds matching records in Freshworks CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `api/search`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Search Records](https://developers.freshworks.com/crm/api/#search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Comma-separated models to include (for example: contact,lead,sales_account,deal). |
| `q` | query | `string` | no | Text query to search for records. |
