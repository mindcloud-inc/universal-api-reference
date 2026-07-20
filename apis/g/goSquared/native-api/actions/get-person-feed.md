# Get Person Feed with GoSquared

Retrieves a person's feed events from GoSquared.

## Endpoint

- **Method:** `GET`
- **Path:** `people/v1/people/:personID/feed`
- **Base URL:** `https://api.gosquared.com`
- **Official documentation:** [Get Person Feed](https://www.gosquared.com/docs/people/people/)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `personID` | path | `string` | yes | The unique identifier of the person whose feed should be retrieved. |
| `query` | query | `string` | no | The query term used to search through the person's event history. |
| `type` | query | `string` | no | Comma-delimited event types to include in the feed. |
| `from` | query | `string` | no | The start date-time for the feed query. |
| `to` | query | `string` | no | The end date-time for the feed query. |
