# List Combo Deals with Gainium

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/deals/combo`
- **Base URL:** `https://api.gainium.io`
- **Official documentation:** [List Combo Deals](https://api.gainium.io/api/docs/v2#/Deals%20-%20Combo/getComboDeals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | query | `string` | no | Filter by bot UUID. |
| `fields` | query | `string` | no | Field selection preset or custom field list. |
| `page` | query | `number` | no | 1-based page number. |
| `status` | query | `list` | no | Filter by deal status. Accepted values: `0`, `1`, `2`, `3`, `4`. |
