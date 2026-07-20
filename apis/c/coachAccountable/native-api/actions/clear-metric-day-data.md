# Clear Metric Day Data with CoachAccountable

Clears metric day data in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Clear Metric Day Data](https://www.coachaccountable.com/APIDocs#Metric.clearDayData)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MetricID` | body | `number` | yes | ID of the Metric to which data is to be cleared. |
| `dateOf` | body | `date` | yes | — |
