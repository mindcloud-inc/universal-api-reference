# Get Tracker Results By Tracker ID with Ship24

Retrieves tracking results for a Ship24 tracker ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v1/trackers/:trackerId/results`
- **Base URL:** `https://api.ship24.com`
- **Official documentation:** [Get Tracker Results By Tracker ID](https://docs.ship24.com/tracking-api-reference/#/operations/get-tracking-results-of-tracker-by-trackerId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackerId` | path | `string` | yes | Ship24 tracker ID returned when the tracker was created. |
