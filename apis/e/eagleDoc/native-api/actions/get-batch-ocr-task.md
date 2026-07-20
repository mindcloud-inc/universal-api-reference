# Get Batch OCR Task with Eagle Doc

Retrieves a batch OCR task from Eagle Doc.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/doc/task/v1`
- **Base URL:** `https://de.eagle-doc.com`
- **Official documentation:** [Get Batch OCR Task](https://www.eagle-doc.com/en/documentation/batch-ocr/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | query | `string` | yes | Batch task ID returned by Eagle Doc when the batch job was created |
