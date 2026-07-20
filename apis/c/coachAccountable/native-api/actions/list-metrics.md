# List Metrics with CoachAccountable

Retrieves metrics from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Metrics](https://www.coachaccountable.com/APIDocs#Metric.getAll)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | The Client whose Metrics are to be gotten. |
| `includeCompleted` | body | `boolean` | no | Set to true to include Metrics that have already been marked complete, otherwise complete Metrics will be omitted. |
| `includeData` | body | `boolean` | no | Set to false in order to omit dataSet from the return value. |
