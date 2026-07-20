# List Documents with Clicksign

Retrieves documents from a Clicksign envelope.

## Endpoint

- **Method:** `GET`
- **Path:** `/envelopes/:envelope_id/documents`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [List Documents](https://developers.clicksign.com/reference/api-listar-documentos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
