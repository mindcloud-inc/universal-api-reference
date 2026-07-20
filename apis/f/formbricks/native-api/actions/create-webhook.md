# Create Webhook with Formbricks

Creates a new webhook in Formbricks.

## Endpoint

- **Method:** `POST`
- **Path:** `/management/webhooks`
- **Base URL:** `https://app.formbricks.com/api/v2`
- **Official documentation:** [Create Webhook](https://formbricks.com/docs/api-v2-reference/management-api--webhooks/create-a-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the webhook. |
| `url` | body | `string` | yes | The destination URL of the webhook. |
| `source` | body | `string` | yes | The source of the webhook. |
| `environmentId` | body | `string` | yes | The environment ID that owns the webhook. |
| `triggers[]` | body | `array<string>` | yes | Webhook trigger types. |
| `surveyIds[]` | body | `array<string>` | yes | Survey IDs associated with the webhook. |
