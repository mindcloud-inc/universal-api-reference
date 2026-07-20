# Upload Email List with EmailListVerify

Uploads an email list for verification in EmailListVerify.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/verifyApiFile`
- **Base URL:** `https://api.emaillistverify.com`
- **Official documentation:** [Upload Email List](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/verifyApiFile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_contents` | body | `file` | yes | CSV, TXT, or XLSX file containing one email address per row. |
| `quality` | body | `string` | no | Bulk verification quality. Standard costs 1 credit per email; high costs 2 credits per email. Accepted values: `0`, `1`. |
