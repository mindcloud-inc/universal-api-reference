# List Webhooks with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/webhook`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [List Webhooks](https://circleci.com/docs/api/v2/#tag/Webhook/operation/getWebhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scope-id` | query | `string` | yes | Project UUID used as the webhook scope. |
| `scope-type` | query | `string` | yes | Webhook scope type. CircleCI currently supports project. |
