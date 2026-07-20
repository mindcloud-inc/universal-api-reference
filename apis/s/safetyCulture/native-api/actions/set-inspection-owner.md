# Set Inspection Owner with SafetyCulture

Updates an inspection owner in SafetyCulture.

## Endpoint

- **Method:** `PUT`
- **Path:** `/inspections/v1/inspections/{inspection_id}/owner`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Set Inspection Owner](https://developer.safetyculture.com/reference/inspectionservice_setowner)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inspection_id` | path | `string` | yes | The unique identifier for the inspection |
| `owner_id` | body | `string` | yes | The unique identifier for the new owner |
