# Create Webhook with Universal API

Creates a new webhook in Universal API.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/webhooks`
- **Base URL:** `https://api.prod.universalapi.io`
- **Official documentation:** [Create Webhook](https://docs.universalapi.io/reference/create-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `unifiedApi` | body | `list<string>` | yes | Unified API category for the webhook. Accepted values: `ATS`, `HRIS`. |
| `deliveryUrl` | body | `string` | yes | Webhook delivery URL. |
| `status` | body | `list<string>` | yes | Webhook status. Accepted values: `Disabled`, `Enabled`. |
| `events[]` | body | `array<string>` | yes | Webhook event names. |
