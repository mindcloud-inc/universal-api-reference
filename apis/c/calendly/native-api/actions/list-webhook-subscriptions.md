# List Webhook Subscriptions with Calendly

Retrieves webhook subscriptions from Calendly.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhook_subscriptions`
- **Base URL:** `https://api.calendly.com`
- **Official documentation:** [List Webhook Subscriptions](https://developer.calendly.com/receive-data-from-scheduled-events-in-real-time-with-webhook-subscriptions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization` | query | `list` | yes | Organization URI filter. Accepted values: `https://api.calendly.com/organizations/e684df12-9454-43ef-8fc4-2d0faa4ec21e`. |
| `scope` | query | `list` | yes | Scope for webhook subscription lookup. Accepted values: `organization`, `user`. |
