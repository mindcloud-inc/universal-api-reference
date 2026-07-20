# Create Prospect with Teach 'n Go

Creates a new prospect in Teach 'n Go.

## Endpoint

- **Method:** `POST`
- **Path:** `/LeadsApi/add`
- **Base URL:** `https://app.teachngo.com`
- **Official documentation:** [Create Prospect](https://intercom.help/teach-n-go/en/articles/5750592-prospect-registration-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `school_id` | body | `string` | yes | Your Teach 'n Go school ID. |
| `fname` | body | `string` | yes | The prospect's first name. |
| `lname` | body | `string` | yes | The prospect's surname. |
| `mobile_phone` | body | `string` | no | The prospect's contact number. |
| `email_address` | body | `string` | no | The prospect's email address. |
| `description` | body | `string` | no | Additional information to capture about the prospect. |
| `gender` | body | `string` | no | Male, Female, or Not specified. |
| `date_of_birth` | body | `date` | no | The prospect's date of birth. |
| `course_subject` | body | `string` | no | The student's chosen subject. |
| `course_level` | body | `string` | no | The student's chosen level. |
