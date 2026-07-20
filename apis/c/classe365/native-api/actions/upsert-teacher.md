# Upsert Teacher with Classe365

Creates or updates a teacher in Classe365.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/teacher`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Upsert Teacher](https://speca.io/classe365/academics#insert-update-teacher)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | no | Teacher first name. |
| `gender` | body | `string` | no | Teacher gender. |
| `id` | body | `string` | no | Teacher id for updates. |
| `is_academic` | body | `string` | no | 1 for academic teacher. |
| `last_name` | body | `string` | no | Teacher last name. |
| `teacher_contact` | body | `string` | no | Teacher contact number. |
| `teacher_dob` | body | `string` | no | Teacher date of birth in YYYY-MM-DD. |
| `teacher_email` | body | `string` | no | Teacher email. |
| `teacher_id` | body | `string` | no | Teacher code/identifier. |
