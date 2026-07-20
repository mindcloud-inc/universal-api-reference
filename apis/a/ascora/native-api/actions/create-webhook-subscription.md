# Create Webhook Subscription with Ascora

Creates a new webhook subscription in Ascora.

## Endpoint

- **Method:** `POST`
- **Path:** `/WebHooks`
- **Base URL:** `https://api.ascora.com.au`
- **Official documentation:** [Create Webhook Subscription](https://www.dropbox.com/scl/fi/75586ygs35arfb7d3cvxi/API-Endpoints-1.2.pdf?rlkey=ztci7pf4nuasegnybjreqsqe2&dl=0#page=69)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hookUrl` | body | `string` | yes | Full URL endpoint Ascora should call when the event is triggered. |
| `systemName` | body | `string` | yes | Name of the external system subscribing to the event. |
| `hookEvent` | body | `string` | yes | Name of the webhook event to subscribe to. |
