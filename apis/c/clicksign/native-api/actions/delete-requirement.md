# Delete Requirement with Clicksign

Deletes an existing requirement from Clicksign.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/envelopes/:envelope_id/requirements/:requirement_id`
- **Base URL:** `https://app.clicksign.com/api/v3`
- **Official documentation:** [Delete Requirement](https://developers.clicksign.com/reference/api-excluir-requisito)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `envelope_id` | path | `string` | yes | The UUID of the envelope. |
| `requirement_id` | path | `string` | yes | The UUID of the requirement. |
