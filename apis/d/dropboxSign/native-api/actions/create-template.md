# Create Template with Dropbox Sign

Creates a template in Dropbox Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/template/create`
- **Base URL:** `https://api.hellosign.com/v3`
- **Official documentation:** [Create Template](https://developers.hellosign.com/api/template/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_urls[]` | body | `array<string>` | yes | Public file URLs Dropbox Sign should download for the template. |
| `title` | body | `string` | yes | Template title. |
| `subject` | body | `string` | no | Default template email subject. |
| `message` | body | `string` | no | Default template email message. |
| `test_mode` | body | `boolean` | no | Whether the template should be created in test mode. |
| `signer_roles[].name` | body | `string` | yes | Signer role name. |
| `signer_roles[].order` | body | `number` | yes | Signer role order. |
| `form_fields_per_document[].document_index` | body | `number` | yes | Document index for the form field. |
| `form_fields_per_document[].api_id` | body | `string` | yes | Unique API id for the form field. |
| `form_fields_per_document[].type` | body | `string` | yes | Form field type. |
| `form_fields_per_document[].required` | body | `boolean` | yes | Whether the field is required. |
| `form_fields_per_document[].signer` | body | `string` | yes | Signer index for the field. |
| `form_fields_per_document[].width` | body | `number` | yes | Field width. |
| `form_fields_per_document[].height` | body | `number` | yes | Field height. |
| `form_fields_per_document[].x` | body | `number` | yes | Field x coordinate. |
| `form_fields_per_document[].y` | body | `number` | yes | Field y coordinate. |
| `form_fields_per_document[].page` | body | `number` | yes | Field page number. |
