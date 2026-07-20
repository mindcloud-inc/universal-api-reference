# Create Account Custom Field with Ortto

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/custom-field/create`
- **Base URL:** `{apiBaseUrl}/v1`
- **Official documentation:** [Create Account Custom Field](https://help.ortto.com/a-265-create-a-custom-field-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Ortto custom field type such as text, integer, or single_select. |
| `name` | body | `string` | yes | Internal custom field name. Ortto requires this and does not accept display_name for creation. |
| `values[]` | body | `array<string>` | no | Option values for select-style custom fields. Send multiple values as a array separated by `,`. |
| `track_changes` | body | `boolean` | no | Whether Ortto should retain change history for this field. |
