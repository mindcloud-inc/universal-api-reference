# List Cases with Docsumo

Retrieves cases for a Docsumo case type.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/external/agents/:casetype_id/cases`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [List Cases](https://support.docsumo.com/reference/get-cases-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `casetype_id` | path | `string` | yes | Docsumo case type ID. |
