# Process Business Card with Abbyy

Creates a business card OCR task in ABBYY Cloud OCR SDK.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/processBusinessCard`
- **Base URL:** `https://cloud-westus.ocrsdk.com`
- **Official documentation:** [Process Business Card](https://support.abbyy.com/hc/en-us/articles/360017269740-processBusinessCard-Method)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Business card image or PDF file to process. |
