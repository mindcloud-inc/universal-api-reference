# Add Digital Signature Field with SigningHub

Adds a digital signature field in SigningHub.

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/packages/:packageId/documents/:documentId/fields/signature`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Add Digital Signature Field](https://manuals.nsignhub.com/latest/Api/#tag/Document-Preparation/operation/V4_Signature_AddSignature)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | The package ID for which the field is being added. |
| `documentId` | path | `number` | yes | The document ID where the field is to be added. |
| `order` | body | `number` | yes | Workflow recipient order for the signature field. |
| `page_no` | body | `number` | yes | Document page number where the field will be added. |
| `field_name` | body | `string` | no | Optional field name. If omitted, SigningHub assigns one automatically. |
| `level_of_assurance` | body | `string` | yes | Signature assurance level, for example ELECTRONIC_SIGNATURE. |
| `display` | body | `string` | no | Visibility of the field, VISIBLE or INVISIBLE. |
| `x` | body | `number` | yes | Left position of the field in pixels. |
| `y` | body | `number` | yes | Top position of the field in pixels. |
| `width` | body | `number` | yes | Field width in pixels. |
| `height` | body | `number` | yes | Field height in pixels. |
