# Regenerate Webhook Secret with SWELLEnterprise

Regenerates a webhook secret in SWELLEnterprise.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/subscriptions/:id/regenerate-secret`
- **Base URL:** `https://dashboard.swellsystem.com/api/v1`
- **Official documentation:** [Regenerate Webhook Secret](https://dashboard.swellsystem.com/docs#webhooks-POSTapi-v1-webhooks-subscriptions--id--regenerate-secret)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The webhook subscription ID. |
