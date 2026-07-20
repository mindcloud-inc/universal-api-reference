# List Filled Forms with PdfFiller

Retrieves filled forms from a PdfFiller fill request.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/fillable_forms/:linkToFillId/filled_forms`
- **Base URL:** `https://api.pdffiller.com`
- **Official documentation:** [List Filled Forms](https://pdffiller.readme.io/reference/get_v2-fillable-forms-link-to-fill-id-filled-forms)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `link_to_fill_id` | path | `string` | yes |
