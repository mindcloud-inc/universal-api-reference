# List Facebook Pages with Marketing Master IO

Retrieves imported Facebook pages from Marketing Master IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/facebook_pages`
- **Base URL:** `https://api.marketingmaster.io`
- **Official documentation:** [List Facebook Pages](https://developers.marketingmaster.io/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enabled` | query | `string` | no | Set to 1 for enabled pages or 0 for disabled pages. |
