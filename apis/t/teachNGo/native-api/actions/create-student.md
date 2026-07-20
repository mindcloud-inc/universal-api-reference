# Create Student with Teach 'n Go

Creates a new student in Teach 'n Go.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/student`
- **Base URL:** `https://app.teachngo.com`
- **Official documentation:** [Create Student](https://intercom.help/teach-n-go/en/articles/6807235-new-student-and-class-registration-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fname` | body | `string` | yes | The student's first name. |
| `lname` | body | `string` | yes | The student's last name. |
| `email_address` | body | `string` | no | The student's email address. |
| `mobile_phone` | body | `string` | no | The student's mobile phone number. |
| `gender` | body | `string` | no | Male, Female, or Not specified. |
| `date_of_birth` | body | `date` | no | The student's date of birth. |
| `registration_date` | body | `date` | no | The date the student was registered. |
