# Create Template with Koncile OCR

## Endpoint

- **Method:** `POST`
- **Path:** `/create_template`
- **Base URL:** `https://api.koncile.ai/v1`
- **Official documentation:** [Create Template](https://docs.koncile.ai/api-setup/templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_locale` | body | `string` | no | Locale for date formatting, such as EU or US. |
| `desc` | body | `string` | no | A description of the template. |
| `folder_id` | body | `number` | yes | The folder identifier the template belongs to. |
| `name` | body | `string` | yes | The template name to create. |
| `number_locale` | body | `string` | no | Locale for number formatting, such as EU or US. |
| `template_id` | query | `number` | no | Copy an existing template into the new template when provided. |
