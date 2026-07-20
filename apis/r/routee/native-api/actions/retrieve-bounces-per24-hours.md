# Retrieve bounces per 24 hours with Routee

Retrieves bounces per 24 hours from Routee.

## Endpoint

- **Method:** `GET`
- **Path:** `/smtp/bounces/day`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Retrieve bounces per 24 hours](https://docs.routee.net/reference/retrieving-bounces-per-24-hours)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `day` | query | `string` | no | The day you want to get information about. Format: YYYY-MM-DD |
| `limit` | query | `string` | no | Number of entries |
| `offset` | query | `string` | no | Sample offset |
