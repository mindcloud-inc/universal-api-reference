# Update Form with Weavely

Updates an existing form in Weavely.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:id`
- **Base URL:** `https://api.weavely.ai/v1`
- **Official documentation:** [Update Form](https://help.weavely.ai/developers/forms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the form to update. |
| `name` | body | `string` | no | Update the form name. |
| `formJSON` | body | `object` | no | Update the form structure containing pages and elements. |
| `themeJSON` | body | `object` | no | Update the form visual theme configuration. |
| `settings` | body | `object` | no | Update form settings. |
| `logicRules[]` | body | `array<object>` | no | Update conditional logic rules. |
| `eventTriggers[]` | body | `array<object>` | no | Update event-based triggers. |
| `calculatedValues[]` | body | `array<object>` | no | Update calculated field values. |
