# Attach a file to a transaction with Lunch Money

## Endpoint

- **Method:** `POST`
- **Path:** `/transactions/:transaction_id/attachments`
- **Base URL:** `https://api.lunchmoney.dev/v2`
- **Official documentation:** [Attach a file to a transaction](https://alpha.lunchmoney.dev/v2/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `transaction_id` | path | `number` | yes |
| `file` | body | `file` | yes |
| `notes` | body | `string` | no |
