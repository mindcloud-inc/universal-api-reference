# Compare Documents (JSON, Uploads) with Diffchecker

Compares documents in Diffchecker and returns a JSON diff from uploads.

## Endpoint

- **Method:** `POST`
- **Path:** `/pdf`
- **Base URL:** `https://api.diffchecker.com/public`
- **Official documentation:** [Compare Documents (JSON, Uploads)](https://www.diffchecker.com/docs/document/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `left_pdf` | body | `file` | yes | Left PDF upload. |
| `right_pdf` | body | `file` | yes | Right PDF upload. |
