# Delete Signer with Clicksign

Deletes an existing signer from Clicksign.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/envelopes/:envelope_id/signers/:signer_id`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [Delete Signer](https://developers.clicksign.com/reference/api-excluir-signatario)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
| `signer_id` | path | `string` | yes | The UUID of the signer. |
