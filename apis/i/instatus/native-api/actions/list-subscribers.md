# List Subscribers with Instatus

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/:page_id/subscribers`
- **Base URL:** `https://api.instatus.com`
- **Official documentation:** [List Subscribers](https://instatus.com/help/api/subscribers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_id` | path | `string` | yes | Instatus status page ID. |
| `search` | query | `string` | no | Search subscribers by email address or phone number. |
