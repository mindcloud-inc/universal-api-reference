# Create or Import Subscription with Pushpad

Creates or imports a subscription into a Pushpad project.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/subscriptions`
- **Base URL:** `https://pushpad.xyz/api/v1`
- **Official documentation:** [Create or Import Subscription](https://pushpad.xyz/docs/rest_api#subscriptions_api_docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `auth` | body | `string` | no | — |
| `endpoint` | body | `string` | yes | — |
| `p256dh` | body | `string` | no | — |
| `project_id` | path | `number` | yes | — |
| `tags[]` | body | `array<string>` | no | Send multiple values as a array. |
| `uid` | body | `string` | no | — |
