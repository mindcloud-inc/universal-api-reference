# Fill Form Fields with SigningHub

Fills form fields in SigningHub.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v4/packages/:packageId/documents/:documentId/fields`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Fill Form Fields](https://manuals.nsignhub.com/latest/Api/#tag/Document-Processing/operation/V4_Fields_FillFormFields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | The document package containing the form fields to fill. |
| `documentId` | path | `number` | yes | The document containing the form fields to fill. |
| `auto_save` | body | `boolean` | no | Whether to save the filled field values automatically. |
| `text[]` | body | `array<object>` | no | Text field values to fill, using objects with field_name and value. |
| `radio[]` | body | `array<object>` | no | Radio field values to fill, using objects supported by SigningHub. |
| `checkbox[]` | body | `array<object>` | no | Checkbox field values to fill, using objects supported by SigningHub. |
| `dropdown[]` | body | `array<object>` | no | Dropdown field values to fill, using objects supported by SigningHub. |
| `listbox[]` | body | `array<object>` | no | Listbox field values to fill, using objects supported by SigningHub. |
