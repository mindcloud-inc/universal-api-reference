# Get Webhook Secret with Localazy

Retrieves the webhook secret from a Localazy project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/webhooks/secret`
- **Base URL:** `https://api.localazy.com`
- **Official documentation:** [Get Webhook Secret](https://localazy.com/docs/api/webhooks-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | Localazy project identifier or slug. |
