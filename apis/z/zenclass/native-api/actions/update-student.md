# Update student with Zenclass

Updates an existing student profile in Zenclass.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/student`
- **Base URL:** `https://api.zenclass.net`
- **Official documentation:** [Update student](https://docs.zenclass.ru)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.city` | body | `string` | no | Updated city. |
| `data.email` | body | `string` | no | New student email address. |
| `data.first_name` | body | `string` | no | Updated first name. |
| `data.last_name` | body | `string` | no | Updated last name. |
| `data.phone` | body | `string` | no | Updated phone number. |
| `email` | body | `string` | yes | Existing student email address. |
