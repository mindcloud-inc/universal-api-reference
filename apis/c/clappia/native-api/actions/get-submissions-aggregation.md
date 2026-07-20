# Get Submissions Aggregation with Clappia

Retrieves submission aggregation results from Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/submissions/getSubmissionsAggregation`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Get Submissions Aggregation](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `requestingUserEmailAddress` | body | `string` | yes | Email address of the Clappia user on whose behalf aggregation should run. |
| `aggregationDimensions[]` | body | `array<object>` | yes | Array of aggregation dimension objects describing the metrics to calculate. |
| `dimensions[]` | body | `array<object>` | no | Optional array of dimension objects for grouping aggregation results. |
