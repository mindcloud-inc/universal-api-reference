# Update Document with Clicksign

Updates an existing document in Clicksign.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/envelopes/:envelope_id/documents/:document_id`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [Update Document](https://developers.clicksign.com/reference/editar-documento)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | no | JSON:API document wrapper. |
| `data.attributes` | body | `object` | no | Document attributes. |
| `data.attributes.status` | body | `string` | yes | The document status. |
| `data.id` | body | `string` | yes | The UUID of the document in the JSON:API body. |
| `document_id` | path | `string` | yes | The UUID of the document. |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
