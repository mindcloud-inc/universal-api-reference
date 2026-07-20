# List Calls with Channels

Retrieves calls from Channels.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/calls`
- **Base URL:** `https://api.channels.app`
- **Official documentation:** [List Calls](https://developers.channels.app/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | query | `string` | no | Optional lower bound for calls. |
| `dateTo` | query | `string` | no | Optional upper bound for calls. |
| `direction` | query | `string` | no | Optional call direction filter. |
