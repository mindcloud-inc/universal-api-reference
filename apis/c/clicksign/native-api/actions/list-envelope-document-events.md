# List Envelope Document Events with Clicksign

Retrieves events for a Clicksign envelope.

## Endpoint

- **Method:** `GET`
- **Path:** `/envelopes/:envelope_id/events`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [List Envelope Document Events](https://developers.clicksign.com/reference/eventos-do-envelope)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
