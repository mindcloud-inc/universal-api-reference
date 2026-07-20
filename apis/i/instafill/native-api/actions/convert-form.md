# Convert Form with Instafill

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/utils/convert`
- **Base URL:** `https://api.instafill.ai`
- **Official documentation:** [Convert Form](https://docs.instafill.ai/docs/api/utils/convert-form)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `pages` | query | `string` | no |
| `confidence` | query | `number` | no |
| `resolution` | query | `number` | no |
| `allowCheckboxes` | query | `boolean` | no |
| `autoConfirm` | query | `boolean` | no |
| `file` | body | `file` | yes |
| `payload` | body | `object` | no |
