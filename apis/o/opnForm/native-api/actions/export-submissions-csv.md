# Export Submissions CSV with OpnForm

Exports form submissions as CSV from OpnForm.

## Endpoint

- **Method:** `POST`
- **Path:** `/open/forms/:id/submissions/export`
- **Base URL:** `https://api.opnform.com`
- **Official documentation:** [Export Submissions CSV](https://docs.opnform.com/api-reference/submissions/export-submissions-csv)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The numeric ID of the form. |
| `columns` | body | `object` | yes | Object mapping field IDs to booleans for the columns to include in the CSV export. |
