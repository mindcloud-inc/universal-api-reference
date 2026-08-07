# List scorecard summaries with Motive

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/scorecard_summary`
- **Base URL:** `https://api.gomotive.com`
- **Official documentation:** [List scorecard summaries](https://developer-docs.gomotive.com/reference/fetch-a-list-of-the-scorecard-summaries-of-the-companys-vehicles)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `driver_ids` | query | `list<number>` | no | Filter scorecard summaries by one or more driver IDs. Send multiple values as a array. |
| `start_date` | query | `date` | no | Calculate scores from this date onward. |
| `end_date` | query | `date` | no | Calculate scores through this date. |
