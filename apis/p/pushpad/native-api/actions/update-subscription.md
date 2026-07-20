# Update Subscription with Pushpad

Updates a subscription in a Pushpad project.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/projects/:project_id/subscriptions/:subscription_id`
- **Base URL:** `https://pushpad.xyz/api/v1`
- **Official documentation:** [Update Subscription](https://pushpad.xyz/docs/rest_api#subscriptions_api_docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `number` | yes | — |
| `subscription_id` | path | `number` | yes | — |
| `tags[]` | body | `array<string>` | no | Send multiple values as a array. |
| `uid` | body | `string` | no | — |
