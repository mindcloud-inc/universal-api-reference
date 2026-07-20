# Update Account Custom Field with Ortto

## Endpoint

- **Method:** `PUT`
- **Path:** `/organizations/custom-field/update`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Update Account Custom Field](https://help.ortto.com/a-752-updating-custom-fields-via-the-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `field_id` | body | `string` | yes | Ortto custom field identifier such as str:o:favorite-color. |
| `replace_values[]` | body | `array<string>` | no | Replace the full option list for this select-style field. Send multiple values as a array separated by `,`. |
| `add_values[]` | body | `array<string>` | no | Append new options for this select-style field. Send multiple values as a array separated by `,`. |
| `remove_values[]` | body | `array<string>` | no | Remove existing options from this select-style field. Send multiple values as a array separated by `,`. |
| `track_changes` | body | `boolean` | no | Whether Ortto should retain change history for this field. |
