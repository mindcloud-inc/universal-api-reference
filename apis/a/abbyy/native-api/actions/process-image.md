# Process Image with Abbyy

Creates an OCR task from an uploaded image in ABBYY.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/processImage`
- **Base URL:** `https://cloud-westus.ocrsdk.com`
- **Official documentation:** [Process Image](https://support.abbyy.com/hc/en-us/articles/360017269420-API-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Image or PDF file to process with ABBYY OCR. |
