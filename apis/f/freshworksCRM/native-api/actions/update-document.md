# Update Document with Freshworks CRM

Updates an existing document in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/cpq/cpq_documents/:id`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Update Document](https://developers.freshworks.com/crm/api/#update_a_document)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `cpq_document` | body | `object` | yes |
| `cpq_document.amount` | body | `number` | no |
| `cpq_document.stage` | body | `string` | no |
| `cpq_document.valid_till` | body | `string` | no |
| `id` | path | `string` | yes |
