# Check Webhook Connectivity with Explorium

Checks webhook connectivity in Explorium API.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/webhooks/check_connectivity`
- **Base URL:** `https://api.explorium.ai`
- **Official documentation:** [Check Webhook Connectivity](https://developers.explorium.ai/reference/webhooks/check_webhook_connectivity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `partner_id` | body | `string` | yes | The partner identifier used for the webhook connectivity check. |
