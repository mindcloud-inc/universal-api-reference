# List Events with Linkbreakers

Retrieves a list of events from Linkbreakers.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/events`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [List Events](https://linkbreakers.com/help/api/events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `linkId` | query | `string` | no | Filter events to a specific link. |
| `startDate` | query | `date` | no | Inclusive start timestamp for the query window. |
| `endDate` | query | `date` | no | Inclusive end timestamp for the query window. |
| `responseFormat` | query | `string` | no | Desired response format. |
| `include[]` | query | `array<string>` | no | Relationships to include in the response. |
