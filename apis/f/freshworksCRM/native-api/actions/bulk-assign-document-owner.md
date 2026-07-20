# Bulk Assign Document Owner with Freshworks CRM

Updates document owners in Freshworks CRM in bulk.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/cpq/cpq_documents/cpq_documents_bulk_assign`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Bulk Assign Document Owner](https://developers.freshworks.com/crm/api/#bulk_assign_document_owner)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `owner_id` | body | `number` | yes |
| `selected_ids[]` | body | `array<number>` | yes |
