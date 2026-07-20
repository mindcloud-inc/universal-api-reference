# Get Form Field with Formstack

Retrieves a field from a Formstack form.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/fields/:fieldId`
- **Base URL:** `https://www.formstack.com/api/v2025`
- **Official documentation:** [Get Form Field](https://developers.formstack.com/reference/getfielddetails-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `number` | yes | The ID of the form. |
| `fieldId` | path | `number` | yes | The ID of the field. |
