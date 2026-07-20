# Update Subscription with GoDaddy CRM

Updates an existing subscription in GoDaddy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/subscriptions/:subscriptionId`
- **Base URL:** `https://api.godaddy.com`
- **Official documentation:** [Update Subscription](https://developer.godaddy.com/doc/endpoint/subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscriptionId` | path | `string` | yes | Required subscription identifier to update |
| `renewAuto` | body | `boolean` | no | Whether the subscription should renew automatically |
