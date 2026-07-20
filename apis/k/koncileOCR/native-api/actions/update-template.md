# Update Template with Koncile OCR

## Endpoint

- **Method:** `PUT`
- **Path:** `/update_template`
- **Base URL:** `https://api.koncile.ai/v1`
- **Official documentation:** [Update Template](https://docs.koncile.ai/api-setup/templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_locale` | body | `string` | no | Update the date formatting locale. |
| `desc` | body | `string` | no | Update the template description. |
| `name` | body | `string` | no | Update the template name. |
| `number_locale` | body | `string` | no | Update the number formatting locale. |
| `template_id` | query | `number` | yes | The template identifier to update. |
