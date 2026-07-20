# Get Realtime Document with OpenRegister

Retrieves a realtime company document from OpenRegister.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/document`
- **Base URL:** `https://api.openregister.de`
- **Official documentation:** [Get Realtime Document](https://docs.openregister.de/endpoint/document-realtime)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | query | `string` | yes | Company ID to retrieve a realtime document for. |
| `document_category` | query | `string` | yes | Document category to retrieve. |
