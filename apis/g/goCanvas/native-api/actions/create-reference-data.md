# Create Reference Data with GoCanvas

## Endpoint

- **Method:** `POST`
- **Path:** `/reference_data`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Create Reference Data](https://api.gocanvas.com/api/v3/docs#create-reference-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `description` | body | `string` | no | — |
| `department_id` | body | `number` | no | Required when Departments are enabled for the GoCanvas company. |
| `headers[]` | body | `array<string>` | yes | — |
| `rows[]` | body | `array<array>` | yes | An array of row arrays, with values in the same order as Headers. |
| `format` | query | `list<string>` | no | Accepted values: `rows`, `rows_with_index`. |
