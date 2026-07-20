# Add Interview Comment with Hireflix

Creates an interview comment in Hireflix.

## Endpoint

- **Method:** `POST`
- **Path:** `me`
- **Base URL:** `https://api.hireflix.com`
- **Official documentation:** [Add Interview Comment](https://api.hireflix.com/me)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | The Hireflix interview ID. |
| `variables.comment` | body | `string` | yes | The comment to add to the interview. |
