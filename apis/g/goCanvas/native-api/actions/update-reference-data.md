# Update Reference Data with GoCanvas

## Endpoint

- **Method:** `PATCH`
- **Path:** `/reference_data/:referenceDataId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Update Reference Data](https://api.gocanvas.com/api/v3/docs#update-reference-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `referenceDataId` | path | `number` | yes | — |
| `headers[]` | body | `array<string>` | yes | Include gc_row_index to identify existing rows for updates. |
| `rows[]` | body | `array<array>` | yes | Rows with an existing gc_row_index update that row. A blank index, or omitting the index column, adds rows. |
| `delete_rows[]` | body | `array<number>` | no | Row indexes to delete. Retrieve the current dataset with Rows with Index first. |
| `publish_to_customers` | body | `boolean` | no | For partners: propagate updated reference data to customer accounts that have access. |
