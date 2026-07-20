# Create Document with Freshworks CRM

Creates a new document in Freshworks CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/cpq/cpq_documents`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Create Document](https://developers.freshworks.com/crm/api/#create_document)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cpq_document` | body | `object` | yes |
| `cpq_document.amount` | body | `number` | no |
| `cpq_document.contact_id` | body | `number` | no |
| `cpq_document.deal_id` | body | `number` | yes |
| `cpq_document.display_name` | body | `string` | no |
| `cpq_document.document_type` | body | `string` | yes |
| `cpq_document.sales_account_id` | body | `number` | no |
| `cpq_document.stage` | body | `string` | no |
| `cpq_document.valid_till` | body | `string` | no |
