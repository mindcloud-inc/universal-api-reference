# Delete Task with Abbyy

Deletes an existing OCR task from ABBYY Cloud OCR SDK.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/deleteTask`
- **Base URL:** `https://cloud-westus.ocrsdk.com`
- **Official documentation:** [Delete Task](https://support.abbyy.com/hc/en-us/articles/360017269420-API-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | query | `string` | yes | ABBYY OCR task identifier to delete. |
