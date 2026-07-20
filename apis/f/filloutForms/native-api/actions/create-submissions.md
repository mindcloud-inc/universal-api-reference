# Create Submissions with Fillout Forms

Creates submissions for a Fillout form.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:formId/submissions`
- **Base URL:** `https://api.fillout.com/v1/api`
- **API:** rest
- **Official documentation:** [Create Submissions](https://www.fillout.com/help/api-reference/create-submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form ID to create submissions for. |
| `submissions[]` | body | `array<object>` | yes | The list of submissions to create. |
