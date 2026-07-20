# Bulk Upsert Contacts with Freshworks CRM

Finds or creates multiple contacts in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/contacts/bulk_upsert`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Bulk Upsert Contacts](https://developers.freshworks.com/crm/api/#bulk_upsert_contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contacts[]` | body | `array<object>` | yes |
| `contacts[].data` | body | `object` | no |
| `contacts[].data.first_name` | body | `string` | no |
| `contacts[].data.last_name` | body | `string` | no |
| `contacts[].emails` | body | `string` | no |
| `contacts[].id` | body | `string` | no |
