# List Sources with Hightouch

Retrieves sources from Hightouch.

## Endpoint

- **Method:** `GET`
- **Path:** `/sources`
- **Base URL:** `https://api.hightouch.com/api/v1`
- **Official documentation:** [List Sources](https://api.hightouch.io/api/swagger.json)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter sources by name. |
| `slug` | query | `string` | no | Filter sources by slug. |
