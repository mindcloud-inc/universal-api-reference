# Delete Document with Clicksign

Deletes an existing document from Clicksign.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/envelopes/:envelope_id/documents/:document_id`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [Delete Document](https://developers.clicksign.com/reference/api-excluir-documento)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The UUID of the document. |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
