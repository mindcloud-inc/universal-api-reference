# Set Document Review Status with Docsumo

Updates a document's review status in Docsumo.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/pik/review/:doc_id/:actions/`
- **Base URL:** `https://app.docsumo.com`
- **Official documentation:** [Set Document Review Status](https://support.docsumo.com/reference/api-v1-user-document-review-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `actions` | path | `string` | yes | Review action path segment. |
| `doc_id` | path | `string` | yes | Docsumo document ID. |
