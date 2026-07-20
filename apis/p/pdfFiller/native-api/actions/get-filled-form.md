# Get Filled Form with PdfFiller

Retrieves a filled form from PdfFiller.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/fillable_forms/:linkToFillId/filled_forms/:filledFormId`
- **Base URL:** `https://api.pdffiller.com`
- **Official documentation:** [Get Filled Form](https://pdffiller.readme.io/reference/get_v2-fillable-forms-link-to-fill-id-filled-forms-filled-form-id)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `link_to_fill_id` | path | `string` | yes |
| `filled_form_id` | path | `string` | yes |
