# Upsert Student with Classe365

Creates or updates a student in Classe365.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/student`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Upsert Student](https://speca.io/classe365/academics#add-update-student)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `admission_number` | body | `string` | no | Student admission number. |
| `father_name` | body | `string` | no | Father name. |
| `first_name` | body | `string` | no | Student first name. |
| `gender` | body | `string` | no | Student gender. |
| `id` | body | `string` | no | Student id for updates. |
| `last_name` | body | `string` | no | Student last name. |
| `mother_name` | body | `string` | no | Mother name. |
| `parents_contact` | body | `string` | no | Parents contact number. |
| `parents_email` | body | `string` | no | Parents email. |
| `student_contact` | body | `string` | no | Student contact number. |
| `student_dob` | body | `string` | no | Student date of birth in YYYY-MM-DD. |
| `student_email` | body | `string` | no | Student email. |
