# List SWML Webhook Addresses with SignalWire

Retrieves SWML webhook addresses from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/fabric/resources/swml_webhooks/{swml_webhook_id}/addresses`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [List SWML Webhook Addresses](https://signalwire.com/docs/apis/rest/swml-webhook/list-swml-webhook-addresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `swml_webhook_id` | path | `string` | yes | Unique ID of a SWML Webhook. |
