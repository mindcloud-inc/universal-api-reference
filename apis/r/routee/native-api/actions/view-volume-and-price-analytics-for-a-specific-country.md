# View Volume and Price Analytics for a specific country with Routee

Retrieves volume and price analytics for a specific country from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/my/volPrice/perMcc`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [View Volume and Price Analytics for a specific country](https://docs.routee.net/reference/view-volumeprice-summary-analytics-for-a-country)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `string` | yes | starting date to get reports |
| `endDate` | query | `string` | yes | ending date to get reports |
| `mcc` | query | `string` | yes | the mcc code |
