# List Subscriptions with Billwerkplus

Retrieves subscriptions from Billwerkplus.

## Endpoint

- **Method:** `GET`
- **Path:** `/list/subscription`
- **Base URL:** `https://api.frisbii.com/v1`
- **Official documentation:** [List Subscriptions](https://docs.frisbii.com/reference/getsubscriptionlist)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `handle` | query | `string` | no | Filter by exact subscription handle. |
| `customer` | query | `string` | no | Filter by customer handle. |
