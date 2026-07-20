# List Signers with Clicksign

Retrieves signers from a Clicksign envelope.

## Endpoint

- **Method:** `GET`
- **Path:** `/envelopes/:envelope_id/signers`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [List Signers](https://developers.clicksign.com/reference/api-listar-signatarios)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
