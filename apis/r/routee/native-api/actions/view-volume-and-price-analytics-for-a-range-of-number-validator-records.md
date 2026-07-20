# View Volume and Price Analytics for a range of Number Validator Records with Routee

Retrieves volume and price analytics for a range of number validator records from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/my/numberValidator/volPrice`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [View Volume and Price Analytics for a range of Number Validator Records](https://docs.routee.net/reference/view-number-validator-volume-and-costs-for-a-specified-date-range)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `date` | yes | starting date to get reports |
| `endDate` | query | `date` | yes | ending date to get reports |
