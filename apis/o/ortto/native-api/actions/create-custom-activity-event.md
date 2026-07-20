# Create Custom Activity Event with Ortto

## Endpoint

- **Method:** `POST`
- **Path:** `/activities/create`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Create Custom Activity Event](https://help.ortto.com/a-271-create-a-custom-activity-event-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activities[]` | body | `array<object>` | yes | Array of activity events to create. |
| `merge_by[]` | body | `array<string>` | no | Person field IDs used to find or create the associated person. |
| `async` | body | `boolean` | no | Queue the activity event asynchronously. |
