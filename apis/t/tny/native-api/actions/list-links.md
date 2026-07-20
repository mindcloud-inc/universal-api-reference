# List Links with Tny

Retrieves short links from Tny.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/links`
- **Base URL:** `https://www.tny.dev`
- **Official documentation:** [List Links](https://www.tny.dev/api-docs#list-links)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scope` | query | `list` | no | Return links for the current API key only or for all API keys on the account. Accepted values: `all`, `key`. |
