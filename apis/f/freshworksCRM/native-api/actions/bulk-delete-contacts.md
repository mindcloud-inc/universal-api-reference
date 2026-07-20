# Bulk Delete Contacts with Freshworks CRM

Deletes multiple contacts from Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/contacts/bulk_destroy`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Bulk Delete Contacts](https://developers.freshworks.com/crm/api/#bulk_delete_contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `selected_ids[]` | body | `array<number>` | yes |
