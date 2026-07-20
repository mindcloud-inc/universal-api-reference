# List Screenshots with Postmaster+

Retrieves screenshots from the Postmaster+ API.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/screenshots`
- **Base URL:** `https://postmasterplus.app`
- **Official documentation:** [List Screenshots](https://postmasterplus.app/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort` | query | `string` | no | Sort order for screenshots. Supported values: created_at, -created_at, format, -format. Accepted values: `0`, `1`, `2`, `3`. |
