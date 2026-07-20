# Delete Template with Koncile OCR

## Endpoint

- **Method:** `DELETE`
- **Path:** `/delete_template`
- **Base URL:** `https://api.koncile.ai/v1`
- **Official documentation:** [Delete Template](https://docs.koncile.ai/api-setup/templates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `override` | query | `boolean` | no | Force deletion of documents inside this template when true. |
| `template_id` | query | `number` | yes | The template identifier to delete. |
