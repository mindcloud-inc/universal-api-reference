# Upload Attachment to Cell with NocoDB

Uploads an attachment to a NocoDB cell.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v3/data/:baseId/:modelId/records/:recordId/fields/:fieldId/upload`
- **Base URL:** `https://app.nocodb.com`
- **Official documentation:** [Upload Attachment to Cell](https://nocodb.com/apis/v3/data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseId` | path | `string` | yes | Base identifier. |
| `modelId` | path | `string` | yes | Model identifier. |
| `recordId` | path | `string` | yes | Record identifier. |
| `fieldId` | path | `string` | yes | Field identifier. |
| `contentType` | body | `string` | yes | Attachment content type. |
| `file` | body | `string` | yes | Base64-encoded file content. |
| `filename` | body | `string` | yes | Original filename. |
