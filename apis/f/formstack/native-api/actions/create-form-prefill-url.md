# Create Form Prefill URL with Formstack

Generates a prefilled form URL in Formstack.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:formId/prefill`
- **Base URL:** `https://www.formstack.com/api/v2025`
- **Official documentation:** [Create Form Prefill URL](https://developers.formstack.com/reference/createformprefill-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `list<number>` | yes | The ID of the form. |
| `fields[]` | body | `array<object>` | no | Field IDs and values to prefill as raw prefill field objects. |
| `incompletePassword` | body | `string` | no | Password for prefill. |
