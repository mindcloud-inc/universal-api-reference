# Update Submission with Formstack

Updates an existing submission in Formstack.

## Endpoint

- **Method:** `PUT`
- **Path:** `/submissions/:submissionId`
- **Base URL:** `https://www.formstack.com/api/v2025`
- **Official documentation:** [Update Submission](https://developers.formstack.com/reference/editsubmission-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submissionId` | path | `number` | yes | The unique identifier of the submission to edit. |
| `fields[]` | body | `array<object>` | yes | Array of field values to update. |
| `fields[].id` | body | `string` | no | The ID of the field to update. |
| `fields[].value` | body | `object` | no | Provide the Formstack typed field-value object. For text fields use `{ "value": "example text" }`. |
| `read` | body | `list<string>` | no | Flag to mark the submission as read. Accepted values: `false`, `true`. |
| `userAgent` | body | `string` | no | User agent of the submission. |
| `remoteAddr` | body | `string` | no | Remote address of the submission. |
| `paymentStatus` | body | `string` | no | Payment status of the submission. |
| `timestamp` | body | `date` | no | Timestamp of the submission. |
