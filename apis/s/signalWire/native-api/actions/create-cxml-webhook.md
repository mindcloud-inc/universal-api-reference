# Create cXML Webhook with SignalWire

Creates a new cXML webhook in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/resources/cxml_webhooks`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Create cXML Webhook](https://signalwire.com/docs/apis/rest/cxml-webhook/create-cxml-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Name of the CXML Webhook. |
| `used_for` | body | `string` | no | Used for of the CXML Webhook. |
| `primary_request_url` | body | `string` | yes | Primary request url of the CXML Webhook. |
| `primary_request_method` | body | `string` | no | Primary request method of the CXML Webhook. |
| `fallback_request_url` | body | `string` | no | Fallback request url of the CXML Webhook. |
| `fallback_request_method` | body | `string` | no | Fallback request method of the CXML Webhook. |
| `status_callback_url` | body | `string` | no | Status callback url of the CXML Webhook. |
| `status_callback_method` | body | `string` | no | Status callback method of the CXML Webhook. |
