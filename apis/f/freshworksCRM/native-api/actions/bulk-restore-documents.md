# Bulk Restore Documents with Freshworks CRM

Restores multiple documents in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/cpq/cpq_documents/cpq_documents_bulk_restore`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Bulk Restore Documents](https://developers.freshworks.com/crm/api/#bulk_restore_documents)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `selected_ids[]` | body | `array<number>` | yes |
