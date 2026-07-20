# Update Call with Avoma

Updates an existing call in Avoma.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/calls/:external_id/`
- **Base URL:** `https://api.avoma.com`
- **Official documentation:** [Update Call](https://dev.avoma.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `external_id` | path | `string` | yes | External ID of the call to update. |
| `subject` | body | `string` | no | Updated subject of the meeting associated with the call. |
| `meeting_purpose_uuid` | body | `string` | no | Updated meeting type UUID associated with the call. |
| `meeting_outcome_uuid` | body | `string` | no | Updated meeting outcome UUID associated with the call. |
