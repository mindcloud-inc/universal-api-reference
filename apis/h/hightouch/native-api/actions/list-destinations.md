# List Destinations with Hightouch

Retrieves destinations from Hightouch.

## Endpoint

- **Method:** `GET`
- **Path:** `/destinations`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [List Destinations](https://api.hightouch.io/api/swagger.json)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter destinations by name. |
| `slug` | query | `string` | no | Filter destinations by slug. |
