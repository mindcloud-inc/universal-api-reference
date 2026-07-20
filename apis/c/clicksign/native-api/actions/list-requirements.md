# List Requirements with Clicksign

Retrieves requirements from a Clicksign envelope.

## Endpoint

- **Method:** `GET`
- **Path:** `/envelopes/:envelope_id/requirements`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [List Requirements](https://developers.clicksign.com/reference/api-listar-requisitos)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
