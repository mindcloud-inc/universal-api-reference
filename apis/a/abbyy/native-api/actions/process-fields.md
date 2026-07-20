# Process Fields with Abbyy

Processes multiple fields in ABBYY Cloud OCR SDK.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/processFields`
- **Base URL:** `https://cloud-westus.ocrsdk.com`
- **Official documentation:** [Process Fields](https://support.abbyy.com/hc/en-us/articles/360017269520-processFields-Method)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | query | `string` | yes | ABBYY OCR task identifier created by Submit Image. |
| `settingsXml` | body | `string` | yes | ABBYY field-definition XML payload that describes the coordinates and field ids to recognize. |
