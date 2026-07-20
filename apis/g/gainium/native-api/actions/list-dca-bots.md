# List DCA Bots with Gainium

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/bots/dca`
- **Base URL:** `https://api.gainium.io`
- **Official documentation:** [List DCA Bots](https://api.gainium.io/api/docs/v2#/Bots%20-%20DCA/getDCABots)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fields` | query | `string` | no | Field selection preset or custom field list. |
| `page` | query | `number` | no | 1-based page number. |
| `status` | query | `list` | no | Filter by bot status. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`. |
