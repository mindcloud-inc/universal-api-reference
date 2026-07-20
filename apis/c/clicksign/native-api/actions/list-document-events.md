# List Document Events with Clicksign

Retrieves events for a Clicksign document.

## Endpoint

- **Method:** `GET`
- **Path:** `/envelopes/:envelope_id/documents/:document_id/events`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [List Document Events](https://developers.clicksign.com/reference/eventos-de-um-documento)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | The UUID of the document. |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
