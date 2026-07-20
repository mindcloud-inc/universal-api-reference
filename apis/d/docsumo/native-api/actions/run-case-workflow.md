# Run Case Workflow with Docsumo

Triggers a workflow for a Docsumo case.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/external/agents/:casetype_id/case/:case_id/run`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Run Case Workflow](https://support.docsumo.com/reference/run-case-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `case_id` | path | `string` | yes | Docsumo case ID. |
| `casetype_id` | path | `string` | yes | Docsumo case type ID. |
