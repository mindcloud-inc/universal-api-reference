# List Event Data with Umami

## Endpoint

- **Method:** `GET`
- **Path:** `/websites/:websiteId/event-data`
- **Base URL:** `https://api.umami.is/v1`
- **Official documentation:** [List Event Data](https://docs.umami.is/docs/api/events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `websiteId` | path | `string` | yes | The website ID. |
| `startAt` | query | `number` | yes | Timestamp in milliseconds for the start of the reporting range. |
| `endAt` | query | `number` | yes | Timestamp in milliseconds for the end of the reporting range. |
