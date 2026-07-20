# Change Student Status with Classe365

Updates a student's status in Classe365.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/studentStatusUpdate`
- **Base URL:** `https://{username}.classe365.com`
- **Official documentation:** [Change Student Status](https://speca.io/classe365/academics#student-status-change)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | body | `string` | no | Student status such as active or alumni. |
| `student_ids` | body | `string` | no | Comma-separated student ids. |
