# View Time Summary Analytics for a country and a network with Routee

Retrieves time summary analytics for a country and a network from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/my/breakdown/perMccMnc`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [View Time Summary Analytics for a country and a network](https://docs.routee.net/reference/view-time-summary-analytics-for-a-country-and-a-network)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `date` | yes | starting date to get reports |
| `endDate` | query | `date` | yes | ending date to get reports |
| `mcc` | query | `string` | yes | the mcc code |
| `mnc` | query | `string` | yes | the mnc code |
