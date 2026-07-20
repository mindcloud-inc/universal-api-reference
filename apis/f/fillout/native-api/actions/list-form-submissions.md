# List Form Submissions with Fillout

Retrieves form submissions from Fillout.

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:formId/submissions`
- **Base URL:** `https://api.fillout.com/v1/api`
- **Official documentation:** [List Form Submissions](https://fillout.com/help/api-reference/get-all-submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The public identifier of the form. |
