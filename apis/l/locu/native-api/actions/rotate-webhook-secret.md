# Rotate Webhook Secret with Locu

Updates a webhook by rotating its secret in Locu.

## Endpoint

- **Method:** `POST`
- **Path:** `/webhooks/:id/rotate-secret`
- **Base URL:** `https://api.locu.app/api/v1`
- **Official documentation:** [Rotate Webhook Secret](https://locu.app/api/docs#tag/webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Webhook ID to rotate the secret for. |
