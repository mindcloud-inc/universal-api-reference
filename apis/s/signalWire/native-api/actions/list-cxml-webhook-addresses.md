# List cXML Webhook Addresses with SignalWire

Retrieves cXML webhook addresses from SignalWire.

## Endpoint

- **Method:** `GET`
- **Path:** `/fabric/resources/cxml_webhooks/{cxml_webhook_id}/addresses`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [List cXML Webhook Addresses](https://signalwire.com/docs/apis/rest/cxml-webhook/list-cxml-webhook-addresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cxml_webhook_id` | path | `string` | yes | Unique ID of a CXML Webhook. |
