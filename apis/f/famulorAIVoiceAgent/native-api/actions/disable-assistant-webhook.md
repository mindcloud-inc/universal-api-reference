# Disable Assistant Webhook with Famulor AI - Voice Agent

Disables webhook notifications for a Famulor assistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/assistants/disable-webhook`
- **Base URL:** `https://app.famulor.de/api`
- **Official documentation:** [Disable Assistant Webhook](https://docs.famulor.io/en/api-reference/assistants/disable-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assistant_id` | body | `number` | yes | Assistant ID to disable webhooks for. |
