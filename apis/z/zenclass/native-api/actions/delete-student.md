# Delete student with Zenclass

Deletes an existing student profile from Zenclass.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/student`
- **Base URL:** `https://api.zenclass.net`
- **Official documentation:** [Delete student](https://docs.zenclass.ru)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Student email address. |
