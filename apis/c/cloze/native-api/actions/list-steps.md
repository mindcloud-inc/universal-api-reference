# List Steps with Cloze

Retrieves steps from Cloze.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/user/steps`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [List Steps](https://api.cloze.com/api-docs/#/paths/v1-user-steps/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `segment` | query | `string` | no | Project segment filter for steps. |
| `stage` | query | `string` | no | Project stage filter for steps. |
