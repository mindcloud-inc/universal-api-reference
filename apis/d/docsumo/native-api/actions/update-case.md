# Update Case with Docsumo

Updates an existing case in Docsumo.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/external/agents/:casetype_id/case/:case_id`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Update Case](https://support.docsumo.com/reference/update-case)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `approval` | body | `string` | no | Approval decision to set on the case. |
| `assigned_to` | body | `string` | no | User ID to assign the case to. |
| `case_fields` | body | `string` | no | JSON object with case field updates. |
| `case_id` | path | `string` | yes | Docsumo case ID. |
| `casetype_id` | path | `string` | yes | Docsumo case type ID. |
| `stage_id` | body | `string` | no | Target stage ID for the case. |
