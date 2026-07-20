# Add Table Row with Docsumo

Adds an empty row to a Docsumo database table.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/raichu/drop_down/db/addrow/:ddid/`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Add Table Row](https://support.docsumo.com/reference/add-new-line)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ddid` | path | `string` | yes | Docsumo dropdown database identifier. |
| `rows` | body | `string` | yes | JSON array of rows to append to the table. |
