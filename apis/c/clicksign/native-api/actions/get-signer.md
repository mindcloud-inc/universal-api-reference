# Get Signer with Clicksign

Retrieves a signer from Clicksign.

## Endpoint

- **Method:** `GET`
- **Path:** `/envelopes/:envelope_id/signers/:signer_id`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [Get Signer](https://developers.clicksign.com/reference/api-detalhes-do-signatario)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
| `signer_id` | path | `string` | yes | The UUID of the signer. |
