# List Result Logs with Typebot

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/typebots/:typebotId/results/:resultId/logs`
- **Base URL:** `https://app.typebot.io/api`
- **Official documentation:** [List Result Logs](https://docs.typebot.io/api-reference/results/list-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `typebotId` | path | `string` | yes | The Typebot ID. |
| `resultId` | path | `string` | yes | The result ID. |
