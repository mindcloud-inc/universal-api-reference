# Delete Webhook with CircleCI

## Endpoint

- **Method:** `DELETE`
- **Path:** `/webhook/:webhook_id`
- **Base URL:** `https://circleci.com/api/v2`
- **Official documentation:** [Delete Webhook](https://circleci.com/docs/api/v2/#tag/Webhook/operation/deleteWebhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_id` | path | `string` | yes | Opaque webhook identifier. |
