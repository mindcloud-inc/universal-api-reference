# List Channels with Landbot

Retrieves channels from Landbot.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/channels/`
- **Base URL:** `https://api.landbot.io`
- **Official documentation:** [List Channels](https://api.landbot.io/#api-Channels-GetHttpsApiLandbotIoV1Channels)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Filter channels by type. |
| `active` | query | `boolean` | no | Filter channels by active status. |
