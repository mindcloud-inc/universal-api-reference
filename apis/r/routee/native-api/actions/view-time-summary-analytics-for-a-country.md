# View Time Summary Analytics for a country with Routee

Retrieves time summary analytics for a country from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/reports/my/breakdown/perCountry`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [View Time Summary Analytics for a country](https://docs.routee.net/reference/view-time-summary-analytics-for-a-country)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDate` | query | `date` | yes | starting date to get reports |
| `endDate` | query | `date` | yes | ending date to get reports |
| `countryCode` | query | `string` | yes | The country’s code in ISO 3166­1 alpha­2 format |
