# Process Text Field with Abbyy

Creates an OCR task for a text field in ABBYY.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/processTextField`
- **Base URL:** `https://cloud-westus.ocrsdk.com`
- **Official documentation:** [Process Text Field](https://support.abbyy.com/hc/en-us/articles/360017326359-How-to-recognize-text-fields)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Image or PDF file that contains the target text field. |
