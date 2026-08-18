# List Productions With Domain Production Only with Centerpoint

## Endpoint

- **Method:** `GET`
- **Path:** `productions`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[updated_at][gt]` | query | `string` | no | Example: 2025-01-13 10:00:00 |
| `filter[updated_at][lt]` | query | `string` | no | — |
| `include` | query | `string` | no | — |
| `filter[domain]` | query | `string` | no | — |
