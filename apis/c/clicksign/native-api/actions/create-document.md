# Create Document with Clicksign

Creates a document in a Clicksign envelope.

## Endpoint

- **Method:** `POST`
- **Path:** `/envelopes/:envelope_id/documents`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [Create Document](https://developers.clicksign.com/reference/api-upload-documentos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content_base64` | body | `string` | yes | The file contents encoded as base64. |
| `data` | body | `object` | no | JSON:API document wrapper. |
| `data.attributes` | body | `object` | no | Document attributes. |
| `data.attributes.filename` | body | `string` | yes | The file name shown in Clicksign. |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
