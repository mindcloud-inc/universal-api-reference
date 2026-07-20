# Get Subscription with Pushpad

Retrieves a subscription from a Pushpad project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/subscriptions/:subscription_id`
- **Base URL:** `https://pushpad.xyz/api/v1`
- **Official documentation:** [Get Subscription](https://pushpad.xyz/docs/rest_api#subscriptions_api_docs)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
| `subscription_id` | path | `number` | yes |
