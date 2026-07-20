# Get Tracker Results By Client Tracker ID with Ship24

Retrieves tracking results by client tracker ID in Ship24.

## Endpoint

- **Method:** `GET`
- **Path:** `/public/v1/trackers/:trackerId/results`
- **Base URL:** `https://api.ship24.com`
- **Official documentation:** [Get Tracker Results By Client Tracker ID](https://docs.ship24.com/tracking-api-reference/#/operations/get-tracking-results-of-tracker-by-trackerId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trackerId` | path | `string` | yes | Your own client tracker ID value used to look up the tracker. |
