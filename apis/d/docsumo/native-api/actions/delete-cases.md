# Delete Cases with Docsumo

Deletes existing cases from a Docsumo case type.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/external/agents/:casetype_id/cases/bulk/delete`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Delete Cases](https://support.docsumo.com/reference/bulk-delete-cases)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_ids[]` | body | `array<string>` | yes | One or more case IDs to delete. |
| `casetype_id` | path | `string` | yes | Docsumo case type ID. |
