# List Subscriptions with Pushpad

Retrieves subscriptions from a Pushpad project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:project_id/subscriptions`
- **Base URL:** `https://pushpad.xyz/api/v1`
- **Official documentation:** [List Subscriptions](https://pushpad.xyz/docs/rest_api#subscriptions_api_docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | — |
| `per_page` | query | `number` | no | — |
| `project_id` | path | `number` | yes | — |
| `tags[]` | query | `array<string>` | no | Send multiple values as a array. |
| `uids[]` | query | `array<string>` | no | Send multiple values as a array. |
