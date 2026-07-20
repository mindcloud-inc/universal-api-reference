# Expel student from school with Zenclass

Expels a student from your Zenclass school.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/student/expel`
- **Base URL:** `https://api.zenclass.net`
- **Official documentation:** [Expel student from school](https://docs.zenclass.ru)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Student email address. |
