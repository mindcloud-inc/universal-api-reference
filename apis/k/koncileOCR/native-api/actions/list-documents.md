# List Documents with Koncile OCR

## Endpoint

- **Method:** `GET`
- **Path:** `/fetch_documents`
- **Base URL:** `https://api.koncile.ai/v1`
- **Official documentation:** [List Documents](https://docs.koncile.ai/api-setup/documents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | query | `string` | no | Filter documents created on or before this YYYY-MM-DD date. |
| `start_date` | query | `string` | no | Filter documents created on or after this YYYY-MM-DD date. |
