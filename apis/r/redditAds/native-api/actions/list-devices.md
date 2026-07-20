# List Devices with Reddit Lead Ads

Retrieves targetable devices from Reddit Ads.

## Endpoint

- **Method:** `GET`
- **Path:** `/targeting/devices`
- **Base URL:** `https://ads-api.reddit.com/api/v3`
- **Official documentation:** [List Devices](https://ads-api.reddit.com/docs/v3/operations/list-devices)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | Optional device IDs filter. |
