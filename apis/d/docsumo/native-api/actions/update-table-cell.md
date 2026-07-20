# Update Table Cell with Docsumo

Updates a single cell in a Docsumo database table.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/raichu/drop_down/db/update/single/:ddid/`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Update Table Cell](https://support.docsumo.com/reference/update-cell)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ddid` | path | `string` | yes | Docsumo dropdown database identifier. |
| `header` | body | `string` | yes | Column header to update. |
| `new_value` | body | `string` | yes | Replacement cell value. |
| `row_id` | body | `string` | yes | Row ID to update. |
