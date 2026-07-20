# Export Comparison as PDF with Draftable

Creates a PDF export job in Draftable.

## Endpoint

- **Method:** `POST`
- **Path:** `/exports`
- **Base URL:** `https://api.draftable.com/v1`
- **Official documentation:** [Export Comparison as PDF](https://api.draftable.com/reference/exporting-comparisons)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comparison` | body | `string` | yes | The identifier of the comparison to export. |
| `kind` | body | `string` | yes | The export format to generate. Accepted values: `combined`, `left`, `right`, `single_page`. |
| `include_cover_page` | body | `boolean` | no | Whether to include a cover page for combined exports. |
