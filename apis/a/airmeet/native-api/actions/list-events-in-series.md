# List Events in Series with Airmeet

Finds events in an Airmeet event series.

## Endpoint

- **Method:** `GET`
- **Path:** `/event-series/{eventSeriesId}/events`
- **Base URL:** `https://api-gateway-prod.us.airmeet.com/prod`
- **Official documentation:** [List Events in Series](https://help.airmeet.com/support/solutions/articles/82000912150-4-manage-event-series-airmeet-public-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventSeriesId` | path | `string` | yes | The Airmeet event series ID. |
