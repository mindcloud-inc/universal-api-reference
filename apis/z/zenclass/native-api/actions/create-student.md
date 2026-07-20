# Create student with Zenclass

Creates a new student profile in Zenclass.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/student`
- **Base URL:** `https://api.zenclass.net`
- **Official documentation:** [Create student](https://docs.zenclass.ru)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.email` | body | `string` | yes | Student email address. |
| `data.first_name` | body | `string` | no | Student first name. |
| `data.last_name` | body | `string` | no | Student last name. |
| `data.send_email` | body | `boolean` | no | Whether Zenclass should email the student. |
