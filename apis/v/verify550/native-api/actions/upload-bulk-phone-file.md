# Upload Bulk Phone File with Verify550

Uploads a bulk phone file to Verify550.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulkPhoneList`
- **Base URL:** `https://app.verify550.com/api`
- **Official documentation:** [Upload Bulk Phone File](https://verify550.com/documentation/validating-phone-numbers-using-the-verify550-api-2/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | query | `string` | yes | Name to assign to the uploaded bulk phone file. |
| `file_contents` | body | `file` | yes | CSV or text file containing phone numbers for bulk validation. |
| `column` | query | `string` | no | Optional source column name when the uploaded file has multiple phone columns. |
