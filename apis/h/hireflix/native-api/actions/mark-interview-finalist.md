# Mark Interview Finalist with Hireflix

Updates finalist status for an interview in Hireflix.

## Endpoint

- **Method:** `POST`
- **Path:** `me`
- **Base URL:** `https://api.hireflix.com`
- **Official documentation:** [Mark Interview Finalist](https://api.hireflix.com/me)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | The Hireflix interview ID. |
| `variables.finalist` | body | `boolean` | no | Whether the interview should be marked as a finalist. |
