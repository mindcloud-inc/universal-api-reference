# Process Document with Abbyy

Processes submitted images as one document in ABBYY Cloud OCR SDK.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/processDocument`
- **Base URL:** `https://cloud-westus.ocrsdk.com`
- **Official documentation:** [Process Document](https://support.abbyy.com/hc/en-us/articles/360017269420-API-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | query | `string` | yes | ABBYY OCR task identifier created by Submit Image. |
