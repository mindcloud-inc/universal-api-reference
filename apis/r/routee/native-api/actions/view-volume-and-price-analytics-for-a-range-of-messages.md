# View Volume and Price Analytics for a range of Messages with Routee

Retrieves volume and price analytics for a range of messages from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/my/volPrice`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [View Volume and Price Analytics for a range of Messages](https://docs.routee.net/reference/view-volumeprice-summary-analytics-for-a-range-of-messages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `string` | yes | — |
| `startDate` | path | `date` | yes | The starting Date of the request |
| `endDate` | query | `string` | yes | — |
| `endDate` | path | `date` | yes | The ending date of the request |
