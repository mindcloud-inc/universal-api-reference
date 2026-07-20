# Get Case Overview with Docsumo

Retrieves overview details for a Docsumo case.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/external/agents/:casetype_id/case/:case_id`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Get Case Overview](https://support.docsumo.com/reference/get-case-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_id` | path | `string` | yes | Docsumo case ID. |
| `casetype_id` | path | `string` | yes | Docsumo case type ID. |
