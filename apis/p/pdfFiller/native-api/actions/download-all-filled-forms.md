# Download All Filled Forms with PdfFiller

Downloads all filled forms from a PdfFiller fill request.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/fillable_forms/:linkToFillId/download`
- **Base URL:** `https://api.pdffiller.com`
- **Official documentation:** [Download All Filled Forms](https://pdffiller.readme.io/reference/get_v2-fillable-forms-link-to-fill-id-download)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `link_to_fill_id` | path | `string` | yes |
