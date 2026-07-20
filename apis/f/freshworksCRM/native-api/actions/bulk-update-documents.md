# Bulk Update Documents with Freshworks CRM

Updates multiple documents in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/cpq/cpq_documents/cpq_documents_bulk_update`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Bulk Update Documents](https://developers.freshworks.com/crm/api/#bulk_update_documents)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cpq_document` | body | `object` | yes |
| `cpq_document.owner_id` | body | `number` | no |
| `cpq_document.stage` | body | `string` | no |
| `ids[]` | body | `array<number>` | yes |
