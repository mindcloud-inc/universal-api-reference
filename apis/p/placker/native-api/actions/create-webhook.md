# Create Webhook with Placker

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook/:board`
- **Base URL:** `https://api.placker.com`
- **Official documentation:** [Create Webhook](https://placker.com/docs/api/paths/webhook.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `board` | path | `number` | yes | Board ID. |
| `notificationUrl` | body | `string` | yes | Webhook target URL. |
| `events[]` | body | `array<string>` | yes | Event types to subscribe to. |
