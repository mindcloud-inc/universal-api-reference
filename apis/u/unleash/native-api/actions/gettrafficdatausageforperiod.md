# Get Aggregated Traffic Data For A Given Time Period. with Unleash

Retrieves aggregated traffic data for a given time period from Unleash.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/admin/metrics/traffic`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Get Aggregated Traffic Data For A Given Time Period.](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `grouping` | query | `string` | yes | Whether to aggregate the data by month or by day |
| `from` | query | `date` | yes | The starting date of the traffic data usage search in IS:yyyy-MM-dd format |
| `to` | query | `date` | yes | The starting date of the traffic data usage search in IS:yyyy-MM-dd format |
