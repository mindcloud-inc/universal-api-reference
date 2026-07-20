# Create Field with Koncile OCR

## Endpoint

- **Method:** `POST`
- **Path:** `/create_field`
- **Base URL:** `https://api.koncile.ai/v1`
- **Official documentation:** [Create Field](https://docs.koncile.ai/api-setup/fields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | body | `string` | yes | The field format to extract. Koncile currently requires this value; use text unless a specific format is needed. |
| `name` | body | `string` | yes | The field name to create. |
| `template_id` | body | `number` | yes | The template identifier the field belongs to. |
| `type` | body | `string` | yes | Whether the field is extracted once (General fields) or for every line (Line fields). |
