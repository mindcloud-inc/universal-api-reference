# Create Submission with Formstack

Creates a new submission in Formstack.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/:formId/submissions`
- **Base URL:** `https://www.formstack.com/api/v2025`
- **Official documentation:** [Create Submission](https://developers.formstack.com/reference/createsubmission-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `list<number>` | yes | The unique identifier of the form to submit to. |
| `fields[]` | body | `array<object>` | yes | Array of field values to submit. |
| `fields[].id` | body | `string` | no | The ID of the field to populate. |
| `fields[].value` | body | `object` | no | Provide the Formstack typed field-value object. For text fields use `{ "value": "example text" }`. |
| `read` | body | `list<string>` | no | Whether to mark the submission as read upon creation. Accepted values: `false`, `true`. |
| `userAgent` | body | `string` | no | The browser user agent string of the submitter. |
| `remoteAddr` | body | `string` | no | The IP address from which the submission is being made. |
| `latitude` | body | `string` | no | The GPS latitude coordinate if location data is available. |
| `longitude` | body | `string` | no | The GPS longitude coordinate if location data is available. |
| `deviceId` | body | `string` | no | The unique device identifier if available from mobile submissions. |
