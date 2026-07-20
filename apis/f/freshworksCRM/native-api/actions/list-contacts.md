# List Contacts with Freshworks CRM

Retrieves contacts from a view in Freshworks CRM.

## Endpoint

- **Method:** `GET`
- **Path:** `api/contacts/view/:view_id`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [List Contacts](https://developers.freshworks.com/crm/api/#list_all_contacts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `view_id` | path | `number` | no | Numeric view identifier used for list queries. |
