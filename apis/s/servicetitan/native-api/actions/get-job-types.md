# Get Job Types with ServiceTitan

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.servicetitan.io/jpm/v2/tenant/{tenant}/job-types`
- **Base URL:** `https://{baseUrl}/`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | query | `string` | no | What kind of items should be returned (only active items will be returned by default) |
| `ids` | query | `string` | no | — |
