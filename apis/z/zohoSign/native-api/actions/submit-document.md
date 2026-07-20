# Submit Document with Zoho Sign

Submits a document for signature in Zoho Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/requests/:requestId/submit`
- **Base URL:** `https://sign.zoho.com/api/v1`
- **Official documentation:** [Submit Document](https://www.zoho.com/sign/api/document-managment/send-document-for-signature.html)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `requestId` | path | `string` | yes | Zoho Sign request identifier. |
| `data` | body | `object` | yes | Zoho Sign submit payload wrapper. |
| `data.requests` | body | `object` | yes | Submit request details. |
| `data.requests.actions[]` | body | `array<object>` | yes | Recipient rows to submit for signature. |
| `data.requests.actions[].action_id` | body | `string` | no | Existing Zoho Sign action identifier for the recipient row. |
| `data.requests.actions[].action_type` | body | `string` | no | Recipient action type such as SIGN. |
| `data.requests.actions[].signing_order` | body | `number` | no | Sequential order number for the recipient. |
| `data.requests.actions[].verify_recipient` | body | `boolean` | no | Whether Zoho Sign should verify the recipient before signing. |
| `data.requests.actions[].private_notes` | body | `string` | no | Private instructions shown to the recipient. |
| `data.requests.actions[].fields[]` | body | `array<object>` | no | Fields assigned to the recipient. |
| `data.requests.actions[].fields[].field_type_name` | body | `string` | no | Zoho Sign field type name. |
| `data.requests.actions[].fields[].field_category` | body | `string` | no | Field category such as textfield. |
| `data.requests.actions[].fields[].field_label` | body | `string` | no | User-facing field label. |
| `data.requests.actions[].fields[].field_name` | body | `string` | no | Internal field name. |
| `data.requests.actions[].fields[].is_mandatory` | body | `boolean` | no | Whether the field must be completed. |
| `data.requests.actions[].fields[].page_no` | body | `number` | no | Zero-based or provider page index for the field placement. |
| `data.requests.actions[].fields[].document_id` | body | `string` | no | Zoho Sign document identifier for the field placement. |
| `data.requests.actions[].fields[].action_id` | body | `string` | no | Recipient action identifier associated with the field. |
| `data.requests.actions[].fields[].x_coord` | body | `number` | no | Horizontal field position. |
| `data.requests.actions[].fields[].y_coord` | body | `number` | no | Vertical field position. |
| `data.requests.actions[].fields[].abs_height` | body | `number` | no | Absolute field height. |
| `data.requests.actions[].fields[].abs_width` | body | `number` | no | Absolute field width. |
| `data.requests.actions[].fields[].text_property` | body | `object` | no | Text styling properties for supported field types. |
| `data.requests.actions[].fields[].text_property.font` | body | `string` | no | Font family for the field text. |
| `data.requests.actions[].fields[].text_property.font_size` | body | `number` | no | Font size for the field text. |
| `data.requests.actions[].fields[].text_property.font_color` | body | `string` | no | Font color for the field text. |
| `data.requests.actions[].fields[].text_property.max_field_length` | body | `number` | no | Maximum allowed field length. |
| `data.requests.actions[].fields[].text_property.is_bold` | body | `boolean` | no | Whether the field text is bold. |
| `data.requests.actions[].fields[].text_property.is_italic` | body | `boolean` | no | Whether the field text is italic. |
