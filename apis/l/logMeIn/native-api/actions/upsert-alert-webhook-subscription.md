# Upsert Alert Webhook Subscription with LogMeIn

Creates or updates an alert webhook subscription in LogMeIn.

## Endpoint

- **Method:** `PUT`
- **Path:** `/goto-resolve-alerts/v1/subscriptions/:subscriptionId`
- **Base URL:** `https://api.goto.com`
- **Official documentation:** [Upsert Alert Webhook Subscription](https://developer.goto.com/LogMeInResolve/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionId` | path | `string` | yes | Required alert subscription ID scoped to the company and user. |
| `channelData.url` | body | `string` | yes | Webhook target URL for alert deliveries. |
| `channelData.sharedSecret` | body | `string` | yes | Shared secret used by the webhook receiver. |
