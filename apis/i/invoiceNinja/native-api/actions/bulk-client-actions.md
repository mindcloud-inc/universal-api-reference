# Bulk Client Actions with Invoice Ninja

## Endpoint

- **Method:** `POST`
- **Path:** `/clients/bulk`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Bulk Client Actions](https://api-docs.invoicing.co/#tag/clients/operation/bulkClients)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | body | `string` | yes | Bulk action to perform, such as archive, restore, delete, template, assign_group, or bulk_update. |
| `ids[]` | body | `array<string>` | yes | Array of client IDs to include in the bulk action. |
| `column` | body | `string` | no | Required for bulk_update. Invoice Ninja supports columns including public_notes, industry_id, size_id, country_id, and custom_value fields. |
| `new_value` | body | `string` | no | Required for bulk_update. New value to set on the selected column. |
| `include` | query | `string` | no | Optional related records to include in the response, such as contacts, documents, activities, ledger, or system_logs. |
