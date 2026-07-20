# Create Call with Callingly

Creates a call in Callingly.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/calls`
- **Base URL:** `https://api.callingly.com`
- **Official documentation:** [Create Call](https://help.callingly.com/article/38-callingly-api-documentation#create-call)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | body | `number` | no | Agency partner account ID for requests on behalf of a client account. |
| `team_id` | body | `number` | yes | Team that should receive the created call. |
| `first_name` | body | `string` | yes | — |
| `last_name` | body | `string` | yes | — |
| `phone_number` | body | `string` | yes | — |
| `email` | body | `string` | no | — |
| `company` | body | `string` | no | — |
| `category` | body | `string` | no | — |
| `source` | body | `string` | no | — |
| `crm_id` | body | `number` | no | — |
| `scheduled_at` | body | `string` | no | Optional schedule timestamp for the call. |
