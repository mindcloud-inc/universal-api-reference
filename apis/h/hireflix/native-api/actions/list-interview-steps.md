# List Interview Steps with Hireflix

Retrieves steps for an interview in Hireflix.

## Endpoint

- **Method:** `POST`
- **Path:** `me`
- **Base URL:** `https://api.hireflix.com`
- **Official documentation:** [List Interview Steps](https://api.hireflix.com/me)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.id` | body | `string` | yes | The Hireflix interview ID. |
| `variables.stepId` | body | `string` | no | Optionally limit the response to one interview step ID. |
| `variables.stepIndex` | body | `number` | no | Optionally limit the response to one interview step index. |
