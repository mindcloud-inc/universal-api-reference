# Send Survey by Email with Simplesat

Sends a survey by email from Simplesat.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/surveys/:survey_token/email`
- **Base URL:** `https://api.simplesat.io`
- **Official documentation:** [Send Survey by Email](https://developer.simplesat.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey_token` | path | `string` | yes | The token of the survey to send |
| `customer` | body | `object` | no | — |
| `team_member` | body | `object` | no | — |
| `ticket` | body | `object` | no | — |
