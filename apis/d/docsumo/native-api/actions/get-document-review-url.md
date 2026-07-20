# Get Document Review URL with Docsumo

Retrieves a signed document review URL from Docsumo.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/eevee/apikey/review-url/:doc_id/`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Get Document Review URL](https://support.docsumo.com/reference/api-v1-user-documents-review-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `doc_id` | path | `string` | no | Docsumo document ID. |
