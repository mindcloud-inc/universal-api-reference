# Create Email Batch Validation with Verificaremails

Creates an email batch validation in Verificaremails.

## Endpoint

- **Method:** `POST`
- **Path:** `/email/validate/multiple`
- **Base URL:** `https://dashboard.verificaremails.com/myapi`
- **Official documentation:** [Create Email Batch Validation](https://dashboard.verificaremails.com/documentation/index.html?v=6)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | CSV, XLS, XLSX, or TXT file containing the email values to validate. |
| `column` | body | `string` | yes | Column letter or number containing the email values. |
| `sendEmail` | body | `list` | no | Send a completion email when processing finishes. Accepted values: `No`, `Yes`. |
| `callbackUrl` | body | `string` | no | Webhook URL to call after the batch completes. |
