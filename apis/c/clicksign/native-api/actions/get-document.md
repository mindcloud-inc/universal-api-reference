# Get Document with Clicksign

Retrieves a document from Clicksign.

## Endpoint

- **Method:** `GET`
- **Path:** `/envelopes/:envelope_id/documents/:document_id`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [Get Document](https://developers.clicksign.com/reference/detalhes-do-documento)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The UUID of the document. |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
