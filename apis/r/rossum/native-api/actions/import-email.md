# Import Email with Rossum

Imports an email into Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/emails/import`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Import Email](https://rossum.app/api/docs/openapi/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `raw_message` | body | `file` | yes | Raw email data. |
| `recipient` | body | `string` | yes | Inbox email address where the message will be imported. |
