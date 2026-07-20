# Upload Bulk Email File with Easy Email Verification

Creates a bulk verification job in Easy Email Verification.

## Endpoint

- **Method:** `POST`
- **Path:** `/bulk/upload`
- **Base URL:** `https://api.easyemailverification.com/v1`
- **Official documentation:** [Upload Bulk Email File](https://eev.stoplight.io/docs/eev/e29cb418841bc-upload-a-bulk-email-file-for-processing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Text or CSV file containing email addresses. |
