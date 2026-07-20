# Process Checkmark Field with Abbyy

Creates an OCR task for a checkmark field in ABBYY.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/processCheckmarkField`
- **Base URL:** `https://cloud-westus.ocrsdk.com`
- **Official documentation:** [Process Checkmark Field](https://support.abbyy.com/hc/en-us/articles/360017269420-API-reference)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Image or PDF file that contains the target checkmark field. |
