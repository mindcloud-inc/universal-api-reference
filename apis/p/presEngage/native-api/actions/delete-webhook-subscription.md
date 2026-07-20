# Delete Webhook Subscription with PresEngage

Deletes an existing webhook subscription from PresEngage.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/hooks/unsubscribe/:subscriptionId`
- **Base URL:** `https://shared.presengage.com/functions/v1/presengage-api`
- **Official documentation:** [Delete Webhook Subscription](https://developer.presengage.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription_id` | path | `string` | yes | Webhook subscription ID to unsubscribe. |
