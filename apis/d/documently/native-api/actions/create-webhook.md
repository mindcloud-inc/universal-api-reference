# Create Webhook with Documently

Creates a new webhook in Documently.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks`
- **Base URL:** `https://app.documently.io/api`
- **Official documentation:** [Create Webhook](https://app.documently.io/api/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/ld+json` |
| `Content-Type` | `application/ld+json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | no | Whether the webhook is active. |
| `events[]` | body | `array<string>` | no | Webhook event names. |
| `project` | body | `string` | no | Project ID for the webhook. |
| `url` | body | `string` | no | Public callback URL. |
