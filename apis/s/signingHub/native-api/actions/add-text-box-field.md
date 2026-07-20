# Add Text Box Field with SigningHub

Adds a text box field in SigningHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/packages/:packageId/documents/:documentId/fields/text`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Add Text Box Field](https://manuals.nsignhub.com/latest/Api/#tag/Document-Preparation/operation/V4_TextBox_AddTextBox)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | Package ID to which the document is added. |
| `documentId` | path | `number` | yes | The document ID where the text field is to be added. |
| `order` | body | `number` | yes | Workflow recipient order for the text field. |
| `page_no` | body | `number` | yes | Document page number where the field will be added. |
| `field_name` | body | `string` | no | Optional text field name. |
| `type` | body | `string` | yes | Text box type, for example TEXT or DATE. |
| `field_type` | body | `string` | yes | Field type, Text or Number. |
| `max_length` | body | `number` | yes | Maximum allowed text length, between 1 and 9999. |
| `placeholder` | body | `string` | no | Placeholder text shown in the text field. |
| `font.name` | body | `string` | yes | Font name, for example HELVETICA. |
| `font.size` | body | `string` | yes | Font size, for example 12. |
| `x` | body | `number` | yes | Left position of the field in pixels. |
| `y` | body | `number` | yes | Top position of the field in pixels. |
| `width` | body | `number` | yes | Field width in pixels. |
| `height` | body | `number` | yes | Field height in pixels. |
| `multiline` | body | `boolean` | no | Set true to create a multiline text area. |
