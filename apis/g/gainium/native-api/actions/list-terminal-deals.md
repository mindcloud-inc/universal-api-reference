# List Terminal Deals with Gainium

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/deals/terminal`
- **Base URL:** `https://api.gainium.io`
- **Official documentation:** [List Terminal Deals](https://api.gainium.io/api/docs/v2#/Terminal/getTerminalDeals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | query | `string` | no | Filter by bot ID. |
| `fields` | query | `string` | no | Field selection preset or custom field list. |
| `page` | query | `number` | no | 1-based page number. |
| `status` | query | `list` | no | Filter by deal status. Accepted values: `0`, `1`, `2`, `3`, `4`. |
