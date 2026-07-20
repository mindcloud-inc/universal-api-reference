# Get Inspection Details with SafetyCulture

Retrieves inspection details from SafetyCulture.

## Endpoint

- **Method:** `GET`
- **Path:** `/inspections/v1/inspections/{id}/details`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Get Inspection Details](https://developer.safetyculture.com/reference/externalinspectionservice_getinspectiondetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID for the inspection. |
| `include_media_url` | query | `boolean` | no | Whether to include media URLs (and metadata) in the response payload. Optional. Defaults to false. |
