# List campaign contacts with Bulldog-WP

Retrieves campaign contacts from Bulldog-WP.

## Endpoint

- **Method:** `GET`
- **Path:** `/campaigns/{campaignId}/contacts`
- **Base URL:** `https://api.bulldog-wp.co.il/v1`
- **Official documentation:** [List campaign contacts](https://console.bulldog-wp.co.il/docs/specification)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | Campaign ID. |
