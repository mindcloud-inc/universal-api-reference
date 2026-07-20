# Set Inspection Site with SafetyCulture

Updates an inspection site in SafetyCulture.

## Endpoint

- **Method:** `PUT`
- **Path:** `/inspections/v1/inspections/{inspection_id}/site`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Set Inspection Site](https://developer.safetyculture.com/reference/inspectionservice_setinspectionsite)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inspection_id` | path | `string` | yes | The ID of the inspection |
| `site_id` | body | `string` | yes | The ID of the site |
