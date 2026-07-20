# View Volume and Price Analytics for a range of Lookup Records with Routee

Retrieves volume and price analytics for a range of lookup records from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/my/lookup/volPrice`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [View Volume and Price Analytics for a range of Lookup Records](https://docs.routee.net/reference/view-volume-and-price-analytics-for-a-range-of-lookup-records)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `date` | yes | starting date to get reports |
| `endDate` | query | `date` | yes | ending date to get reports |
