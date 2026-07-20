# Disable Assistant Inbound Webhook with Famulor AI - Voice Agent

Disables inbound webhook notifications for a Famulor assistant.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/assistants/disable-inbound-webhook`
- **Base URL:** `https://app.famulor.de/api`
- **Official documentation:** [Disable Assistant Inbound Webhook](https://docs.famulor.io/en/api-reference/assistants/disable-inbound-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assistant_id` | body | `number` | yes | Assistant ID to disable inbound webhooks for. |
