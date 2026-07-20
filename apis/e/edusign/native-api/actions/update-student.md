# Update Student with Edusign

Updates an existing student in Edusign.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/student/`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [Update Student](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `student` | body | `object` | yes | — |
| `student.ID` | body | `string` | yes | Student's ID |
| `student.FIRSTNAME` | body | `string` | yes | Student's first name |
| `student.LASTNAME` | body | `string` | yes | Student's last name |
| `student.EMAIL` | body | `string` | no | Student's email |
| `student.FILE_NUMBER` | body | `string` | no | Student's file number |
| `student.PHOTO` | body | `string` | no | Student's photo |
| `student.HIDDEN` | body | `boolean` | no | Student's hidden status |
| `student.GROUPS[]` | body | `array<string>` | no | — |
| `student.GROUPS[]` | body | `array<string>` | no | — |
| `student.GROUPS[]` | body | `array<string>` | no | — |
| `student.PHONE` | body | `string` | no | Student's phone |
| `student.TRAINING_NAME` | body | `string` | no | Student training's name |
| `student.COMPANY` | body | `string` | no | Student's company |
| `student.TAGS[]` | body | `array<string>` | no | — |
| `student.TAGS[]` | body | `array<string>` | no | — |
| `student.TAGS[]` | body | `array<string>` | no | — |
| `student.API_ID` | body | `string` | no | Student's External Id |
| `student.API_TYPE` | body | `string` | no | name of the connector the student if part of (if he is) |
| `student.BADGE_ID` | body | `string` | no | Student's Badge Id |
| `student.STUDENT_FOLLOWER_ID[]` | body | `array<string>` | no | — |
| `student.STUDENT_FOLLOWER_ID[]` | body | `array<string>` | no | — |
| `student.STUDENT_FOLLOWER_ID[]` | body | `array<string>` | no | — |
| `student.VARIABLES[]` | body | `array<object>` | no | — |
| `student.VARIABLES[]` | body | `array<object>` | no | — |
| `student.VARIABLES[]` | body | `array<object>` | no | — |
