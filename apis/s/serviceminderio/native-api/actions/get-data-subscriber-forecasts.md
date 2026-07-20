# Get Data Subscriber Forecasts with serviceminder.io

Retrieves data subscriber forecasts from ServiceMinder.

## Endpoint

- **Method:** `POST`
- **Path:** `/datasubscriber/forecasts`
- **Base URL:** `https://serviceminder.com/api`
- **Official documentation:** [Get Data Subscriber Forecasts](https://serviceminder.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `FromDate` | body | `date` | no | Forecast start date. |
| `ThroughDate` | body | `date` | no | Forecast end date. |
