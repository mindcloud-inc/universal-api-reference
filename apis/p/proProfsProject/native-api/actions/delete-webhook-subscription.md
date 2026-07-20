# Delete Webhook Subscription with ProProfs Project

Deletes a webhook subscription from ProProfs Project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/hooks/{{subscription_id}}`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [Delete Webhook Subscription](https://help.proprofsproject.com/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subscription_id` | path | `string` | yes | The webhook subscription ID to delete. |
