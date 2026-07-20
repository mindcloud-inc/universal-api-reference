# Add Metric Data with CoachAccountable

Adds metric data in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Add Metric Data](https://www.coachaccountable.com/APIDocs#Metric.addData)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `MetricID` | body | `number` | yes | ID of the Metric to which data is to be added. |
| `dateOf` | body | `date` | yes | — |
| `value` | body | `number` | yes | — |
| `comment` | body | `string` | no | Optional note about this data point. |
