# Start Inspection with SafetyCulture

Creates a new inspection in SafetyCulture.

## Endpoint

- **Method:** `POST`
- **Path:** `/audits`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Start Inspection](https://developer.safetyculture.com/reference/thepubservice_startinspection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | body | `string` | yes | ID of the template to start an inspection from. |
| `header_items[]` | body | `array<object>` | no | The title page items of the inspection. |
| `items[]` | body | `array<object>` | no | The items of the inspection. |
