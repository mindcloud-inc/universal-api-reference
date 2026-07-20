# Upsert Contact with Freshworks CRM

Finds a contact in Freshworks CRM, or creates one if no match is found.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/contacts/upsert`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Upsert Contact](https://developers.freshworks.com/crm/api/#upsert_a_contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact` | body | `object` | yes |
| `contact.first_name` | body | `string` | no |
| `contact.last_name` | body | `string` | no |
| `unique_identifier` | body | `object` | yes |
| `unique_identifier.emails` | body | `string` | yes |
