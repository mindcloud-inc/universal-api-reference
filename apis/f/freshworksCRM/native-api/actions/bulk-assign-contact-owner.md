# Bulk Assign Contact Owner with Freshworks CRM

Updates contact owners in Freshworks CRM in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/contacts/bulk_assign_owner`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Bulk Assign Contact Owner](https://developers.freshworks.com/crm/api/#bulk_assign_contact_owner)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `owner_id` | body | `number` | yes |
| `selected_ids[]` | body | `array<number>` | yes |
