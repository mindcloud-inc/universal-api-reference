# List User Webhooks with Zeplin

Retrieves a list of user webhooks from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/me/webhooks`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List User Webhooks](https://docs.zeplin.dev/reference/getuserwebhooks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Filter by webhook status |
| `url_health` | query | `string` | no | Filter by health of webhook's URL |
