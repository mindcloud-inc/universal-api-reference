# Create Form Submission with Fillout

Creates form submissions in Fillout.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:formId/submissions`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [Create Form Submission](https://fillout.com/help/api-reference/create-submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The public identifier of the form. |
| `submissions[]` | body | `array<object>` | yes | The submissions to create. |
