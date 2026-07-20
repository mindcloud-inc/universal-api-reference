# Get Sessions with Focusmate

Retrieves your Focusmate sessions within a date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/sessions`
- **Base URL:** `https://api.focusmate.com/v1`
- **Official documentation:** [Get Sessions](https://apidocs.focusmate.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start` | query | `date` | yes | Lower limit for the date range as an ISO 8601 date-time with an offset or Z. Sessions partially within the range are included. The range must not exceed 1 year. |
| `end` | query | `date` | yes | Upper limit for the date range as an ISO 8601 date-time with an offset or Z. Sessions partially within the range are included. The range must not exceed 1 year. |
