# Get Task Status with Abbyy

Retrieves the current status of an ABBYY OCR task.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/getTaskStatus`
- **Base URL:** `https://cloud-westus.ocrsdk.com`
- **Official documentation:** [Get Task Status](https://support.abbyy.com/hc/en-us/articles/360017269420-API-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | query | `string` | yes | ABBYY OCR task identifier. |
