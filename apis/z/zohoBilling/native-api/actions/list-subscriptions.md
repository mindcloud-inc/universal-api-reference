# List Subscriptions with Zoho Billing

## Endpoint

- **Method:** `GET`
- **Path:** `/subscriptions`
- **Base URL:** `{api_domain}/billing/v1`
- **Official documentation:** [List Subscriptions](https://www.zoho.com/billing/api/v1/subscription/#list-all-subscriptions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter_by` | query | `string` | no | Filter subscriptions by status or mode, for example `SubscriptionStatus.ACTIVE` or `SubscriptionMode.ONLINE`. |
