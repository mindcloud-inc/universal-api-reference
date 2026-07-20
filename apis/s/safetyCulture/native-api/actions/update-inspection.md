# Update Inspection with SafetyCulture

Updates an inspection in SafetyCulture.

## Endpoint

- **Method:** `PUT`
- **Path:** `/audits/{audit_id}`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [Update Inspection](https://developer.safetyculture.com/reference/thepubservice_updateinspection)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audit_id` | path | `string` | yes | The ID of the inspection to update. |
| `archived` | body | `boolean` | no | Whether to archive or un-archive the inspection. Optional. Defaults to false (un-archive). |
| `header_items[]` | body | `array<object>` | no | The title page items of the inspection. |
| `items[]` | body | `array<object>` | no | The items of the inspection. |
