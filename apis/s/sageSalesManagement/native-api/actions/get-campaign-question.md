# Get Campaign Question with Sage Sales Management

Retrieves a campaign question from Sage Sales Management.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaignQuestions/{{id}}`
- **Base URL:** `https://api.forcemanager.com/api/v4`
- **Official documentation:** [Get Campaign Question](https://developer.forcemanager.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Campaign question ID |
