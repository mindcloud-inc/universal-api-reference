# Bulk Delete Documents with Freshworks CRM

Deletes multiple documents from Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/cpq/cpq_documents/cpq_documents_bulk_delete`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Bulk Delete Documents](https://developers.freshworks.com/crm/api/#bulk_delete_documents)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `selected_ids[]` | body | `array<number>` | yes |
