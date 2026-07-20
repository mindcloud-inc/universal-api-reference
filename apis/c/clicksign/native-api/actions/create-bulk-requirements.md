# Create Bulk Requirements with Clicksign

Creates bulk requirements in a Clicksign envelope.

## Endpoint

- **Method:** `POST`
- **Path:** `/envelopes/:envelope_id/bulk_requirements`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [Create Bulk Requirements](https://developers.clicksign.com/reference/bulk-requirements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `atomic:operations[]` | body | `array<object>` | yes | The JSON:API atomic operations array used for bulk requirement creation. |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
