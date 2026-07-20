# View Volume and Price Analytics for a specific country and Network with Routee

Retrieves volume and price analytics for a specific country and network from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/my/volPrice/perMccMnc`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [View Volume and Price Analytics for a specific country and Network](https://docs.routee.net/reference/view-volume-and-price-analytics-for-a-specific-country)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `string` | yes | starting date to get reports |
| `endDate` | query | `string` | yes | ending date to get reports |
| `mcc` | query | `string` | yes | the mcc code |
| `mnc` | query | `string` | yes | the mnc code |
