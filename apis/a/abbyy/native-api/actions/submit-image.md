# Submit Image with Abbyy

Uploads an image to an ABBYY OCR task, creating one if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/submitImage`
- **Base URL:** `https://cloud-westus.ocrsdk.com`
- **Official documentation:** [Submit Image](https://support.abbyy.com/hc/en-us/articles/360017269700-submitImage-Method)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | Image or PDF file to submit into a reusable ABBYY task. |
