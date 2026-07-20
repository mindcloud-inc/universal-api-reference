# Get Capacity Summary with SuperSend

Retrieves the capacity summary from SuperSend.

## Endpoint

- **Method:** `GET`
- **Path:** `/intelligence/capacity-summary`
- **Base URL:** `https://api.supersend.io/v2`
- **Official documentation:** [Get Capacity Summary](https://api.supersend.io/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | query | `string` | yes | Team UUID (from list teams) |
| `page` | query | `number` | no | Default: 1. |
| `limit` | query | `number` | no | Default: 20. |
| `sortBy` | query | `string` | no | Default: projectedCompletionDays. |
| `sortDirection` | query | `string` | no | Allowed values: asc, desc. Default: asc. |
| `planningFilter` | query | `string` | no | Allowed values: all, active, inactive, finished, no-capacity. Default: all. |
| `search` | query | `string` | no | — |
| `includeCampaignId` | query | `string` | no | When set, response includes focusedCampaign with this campaign's row even if it would not appear on the requested page. |
