# Update Webhook with Roger

## Endpoint

- **Method:** `PATCH`
- **Path:** `/webhooks/:id`
- **Base URL:** `https://api.rogerroger.io`
- **Official documentation:** [Update Webhook](https://developer.rogerroger.io/webhooks/set-up-a-webhook)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/merge-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Webhook identifier. |
| `description` | body | `string` | yes | Updated webhook description. |
