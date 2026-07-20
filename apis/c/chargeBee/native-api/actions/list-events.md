# List Events with ChargeBee

## Endpoint

- **Method:** `GET`
- **Path:** `events`
- **Base URL:** `https://{baseUrl}.chargebee.com/api/v2/`
- **Official documentation:** [List Events](https://apidocs.chargebee.com/docs/api/events/list-events)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event_type[in]` | query | `list<string>` | no | Send multiple values as a string. |
| `occurred_at[after]` | query | `string` | no | — |
