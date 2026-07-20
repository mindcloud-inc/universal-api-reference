# Upload Verification File with MyEmailVerifier

Creates a bulk verification upload in MyEmailVerifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/verifier/upload_file`
- **Base URL:** `https://client.myemailverifier.com`
- **Official documentation:** [Upload Verification File](https://myemailverifier.com/real-time-email-verification)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | body | `file` | yes | Required TXT, CSV, or XLSX file containing one email address per row. |
