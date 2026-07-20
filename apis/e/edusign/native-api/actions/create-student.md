# Create Student with Edusign

Creates a new student in Edusign.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/student`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [Create Student](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `student` | body | `object` | yes | — |
| `student.FIRSTNAME` | body | `string` | yes | Student's first name |
| `student.LASTNAME` | body | `string` | yes | Student's last name |
| `student.EMAIL` | body | `string` | yes | Student's email |
| `student.FILE_NUMBER` | body | `string` | no | — |
| `student.PHOTO` | body | `string` | no | Student's photo |
| `student.PHONE` | body | `string` | no | Student's phone |
| `student.GROUPS[]` | body | `array<string>` | no | — |
| `student.GROUPS[]` | body | `array<string>` | no | — |
| `student.GROUPS[]` | body | `array<string>` | no | — |
| `student.TRAINING_NAME` | body | `string` | no | Student training's name |
| `student.COMPANY` | body | `string` | no | Student's company |
| `student.TAGS[]` | body | `array<string>` | no | — |
| `student.TAGS[]` | body | `array<string>` | no | — |
| `student.TAGS[]` | body | `array<string>` | no | — |
| `student.SEND_EMAIL_CREDENTIALS` | body | `boolean` | no | boolean to know if the API sends the credentials to the mail of the student |
| `student.API_ID` | body | `string` | no | Student's External Id |
| `student.API_TYPE` | body | `string` | no | name of the connector the student if part of (if he is) |
| `student.BADGE_ID` | body | `string` | no | — |
| `student.STUDENT_FOLLOWER_ID[]` | body | `array<string>` | no | — |
| `student.STUDENT_FOLLOWER_ID[]` | body | `array<string>` | no | — |
| `student.STUDENT_FOLLOWER_ID[]` | body | `array<string>` | no | — |
| `student.ISIC_ID` | body | `string` | no | Student's ISIC ID |
| `student.STUDENT_CARD` | body | `object` | no | — |
| `student.STUDENT_CARD.BIRTH_DATE` | body | `string` | no | Student's birth date |
| `student.STUDENT_CARD.DIPLOMA` | body | `string` | no | Student's diploma |
| `student.STUDENT_CARD.STUDENT_NATIONAL_ID` | body | `string` | no | Student's national ID |
| `student.STUDENT_CARD.CARD_EXPIRATION_DATE` | body | `string` | no | Student's card expiration date |
| `student.STUDENT_CARD.SCHOOL_YEAR` | body | `string` | no | Student's school year |
| `student.NEW_PASSWORD_NEEDED` | body | `boolean` | no | Ask the student to change the password on first login (default: true) |
| `student.HIDDEN` | body | `number` | no | Student's hidden status |
