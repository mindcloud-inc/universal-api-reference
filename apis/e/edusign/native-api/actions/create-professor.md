# Create Professor with Edusign

Creates a new professor in Edusign.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/professor`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [Create Professor](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `professor` | body | `object` | yes | — |
| `professor.FIRSTNAME` | body | `string` | yes | Firstname of the professor |
| `professor.LASTNAME` | body | `string` | yes | Lastname of the professor |
| `professor.EMAIL` | body | `string` | yes | Email of the professor |
| `professor.SPECIALITY` | body | `string` | no | Speciality of the professor |
| `professor.API_ID` | body | `string` | no | API ID of the professor |
| `professor.API_TYPE` | body | `string` | no | API type of the professor |
| `professor.TAGS[]` | body | `array<string>` | no | — |
| `professor.TAGS[]` | body | `array<string>` | no | — |
| `professor.PHONE` | body | `string` | no | Phone of the professor |
| `professor.VARIABLES[]` | body | `array<object>` | no | — |
| `professor.VARIABLES[]` | body | `array<object>` | no | — |
| `dontSendCredentials` | body | `boolean` | yes | If true, the credentials won't be sent to the professor |
