# Get Webhook Event Logs with DigiCert

Retrieves event logs for a DigiCert webhook.

## Endpoint

- **Method:** `GET`
- **Path:** `/webhook/:webhook_id/event-logs`
- **Base URL:** `https://www.digicert.com/services/v2`
- **Official documentation:** [Get Webhook Event Logs](https://dev.digicert.com/en/certcentral-apis/services-api/webhooks/webhook-event-logs.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `webhook_id` | path | `string` | yes | The DigiCert webhook identifier. |
