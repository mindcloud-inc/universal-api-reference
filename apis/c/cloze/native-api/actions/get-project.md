# Get Project with Cloze

Retrieves a project from Cloze.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/get`
- **Base URL:** `https://api.cloze.com`
- **Official documentation:** [Get Project](https://api.cloze.com/api-docs/#/paths/v1-projects-get/get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uniqueid` | query | `string` | yes | Project unique direct identifier or custom identifier. |
| `team` | query | `boolean` | no | Retrieve the team relation instead of the local relation. |
| `detailed` | query | `boolean` | no | Retrieve detailed information. |
