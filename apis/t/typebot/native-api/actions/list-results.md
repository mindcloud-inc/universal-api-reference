# List Results with Typebot

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/typebots/:typebotId/results`
- **Base URL:** `https://app.typebot.io/api`
- **Official documentation:** [List Results](https://docs.typebot.io/api-reference/results/list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `typebotId` | path | `string` | yes | The Typebot ID. |
| `timeFilter` | query | `string` | no | Time range filter. |
| `timeZone` | query | `string` | no | Time zone for the time filter. |
| `limit` | query | `number` | no | Maximum number of results to return. |
| `cursor` | query | `number` | no | Cursor for the next results page. |
