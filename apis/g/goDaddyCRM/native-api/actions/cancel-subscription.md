# Cancel Subscription with GoDaddy CRM

Cancels an existing subscription in GoDaddy.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/subscriptions/:subscriptionId`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Cancel Subscription](https://developer.godaddy.com/doc/endpoint/subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionId` | path | `string` | yes | Required subscription identifier to cancel |
