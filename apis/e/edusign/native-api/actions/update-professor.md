# Update Professor with Edusign

Updates an existing professor in Edusign.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/professor/`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [Update Professor](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `professor` | body | `object` | yes | — |
| `professor.ID` | body | `string` | yes | ID of the professor |
| `professor.FIRSTNAME` | body | `string` | yes | Firstname of the professor |
| `professor.LASTNAME` | body | `string` | yes | Lastname of the professor |
| `professor.EMAIL` | body | `string` | yes | Email of the professor |
| `professor.SPECIALITY` | body | `string` | no | Speciality of the professor |
| `professor.API_ID` | body | `string` | no | API ID of the professor |
| `professor.API_TYPE` | body | `string` | no | API type of the professor |
| `professor.TAGS[]` | body | `array<string>` | no | — |
| `professor.TAGS[]` | body | `array<string>` | no | — |
| `professor.PHONE` | body | `string` | no | Phone of the professor |
| `professor.PIN` | body | `string` | no | Pin of the professor |
| `professor.HIDDEN` | body | `string` | no | Hidden of the professor |
| `professor.VARIABLES[]` | body | `array<object>` | no | — |
| `professor.VARIABLES[]` | body | `array<object>` | no | — |
