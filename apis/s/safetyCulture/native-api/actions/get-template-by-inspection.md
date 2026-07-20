# Get Template by Inspection with SafetyCulture

Retrieves a template by inspection in SafetyCulture.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates/v1/templates/inspections/{inspection_id}`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Get Template by Inspection](https://developer.safetyculture.com/reference/templatesservice_gettemplatebyinspectionid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `inspection_id` | path | `string` | yes | The ID for the inspection. |
| `locale` | query | `string` | no | The preferred locale of the template. |
