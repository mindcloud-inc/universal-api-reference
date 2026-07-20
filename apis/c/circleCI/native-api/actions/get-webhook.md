# Get Webhook with CircleCI

## Endpoint

- **Method:** `GET`
- **Path:** `/webhook/:webhook_id`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Get Webhook](https://circleci.com/docs/api/v2/#tag/Webhook/operation/getWebhookById)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_id` | path | `string` | yes | Opaque webhook identifier. |
