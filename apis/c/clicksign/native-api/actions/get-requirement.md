# Get Requirement with Clicksign

Retrieves a requirement from Clicksign.

## Endpoint

- **Method:** `GET`
- **Path:** `/envelopes/:envelope_id/requirements/:requirement_id`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [Get Requirement](https://developers.clicksign.com/reference/detalhes-do-requisito)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
| `requirement_id` | path | `string` | yes | The UUID of the requirement. |
