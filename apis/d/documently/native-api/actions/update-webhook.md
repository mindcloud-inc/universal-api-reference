# Update Webhook with Documently

Updates an existing webhook in Documently.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/webhooks/:webhookId`
- **Base URL:** `https://app.documently.io/api`
- **Official documentation:** [Update Webhook](https://app.documently.io/api/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/ld+json` |
| `Content-Type` | `application/merge-patch+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | no | Whether the webhook is active. |
| `events[]` | body | `array<string>` | no | Webhook event names. |
| `project` | body | `string` | no | Project ID for the webhook. |
| `url` | body | `string` | no | Public callback URL. |
| `webhookId` | path | `string` | no | The webhook id. |
