# Get Usage with Phonely

Retrieves usage from Phonely.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/usage`
- **Base URL:** `https://app.phonely.ai`
- **Official documentation:** [Get Usage](https://docs.phonely.ai/api-reference/endpoint/get-usage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | query | `string` | yes | The Phonely user ID whose usage should be summarized. |
| `startDate` | query | `string` | yes | The inclusive start date for the usage window. |
| `endDate` | query | `string` | yes | The inclusive end date for the usage window. |
| `agentId` | query | `string` | no | Optionally restrict usage results to a single agent. |
