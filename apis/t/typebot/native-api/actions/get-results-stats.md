# Get Results Stats with Typebot

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/typebots/:typebotId/analytics/stats`
- **Base URL:** `https://app.typebot.io/api`
- **Official documentation:** [Get Results Stats](https://docs.typebot.io/api-reference/analytics/get-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `typebotId` | path | `string` | yes | The Typebot ID. |
| `timeFilter` | query | `string` | no | Time range filter. |
| `timeZone` | query | `string` | no | Time zone for the time filter. |
