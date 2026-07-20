# List Monitors with Better Stack Uptime

Retrieves monitors from Better Stack Uptime.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/monitors`
- **Base URL:** `https://uptime.betterstack.com/api`
- **Official documentation:** [List Monitors](https://betterstack.com/docs/uptime/api/list-all-existing-monitors/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | no | Filter monitors by exact URL |
| `pronounceable_name` | query | `string` | no | Filter monitors by Better Stack pronounceable name |
