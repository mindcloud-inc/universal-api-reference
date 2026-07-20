# Create Form with Weavely

Creates a new form in Weavely.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms`
- **Base URL:** `https://api.weavely.ai/v1`
- **Official documentation:** [Create Form](https://help.weavely.ai/developers/forms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Display name for the form shown in the Weavely dashboard. |
| `teamId` | body | `string` | yes | The UUID of the team to associate this form with. |
| `publish` | body | `boolean` | no | Set to true to publish the form immediately. |
| `formJSON` | body | `object` | yes | The form structure containing all pages and elements. |
| `themeJSON` | body | `object` | yes | The form visual theme configuration. |
| `settings` | body | `object` | no | Optional form settings. |
| `logicRules[]` | body | `array<object>` | no | Optional conditional logic rules. |
| `eventTriggers[]` | body | `array<object>` | no | Optional event-based triggers. |
| `calculatedValues[]` | body | `array<object>` | no | Optional calculated field values. |
| `pageAttributes` | body | `object` | no | Optional page-specific attributes. |
