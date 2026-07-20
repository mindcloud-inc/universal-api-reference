# Update cXML Webhook with SignalWire

Updates an existing cXML webhook in SignalWire.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/fabric/resources/cxml_webhooks/{id}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Update cXML Webhook](https://signalwire.com/docs/apis/rest/cxml-webhook/update-cxml-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of a CXML Webhook. |
| `name` | body | `string` | no | Name of the CXML Webhook. |
| `used_for` | body | `string` | no | Used for of the CXML Webhook. |
| `primary_request_url` | body | `string` | no | Primary request url of the CXML Webhook. |
| `primary_request_method` | body | `string` | no | Primary request method of the CXML Webhook. |
| `fallback_request_url` | body | `string` | no | Fallback request url of the CXML Webhook. |
| `fallback_request_method` | body | `string` | no | Fallback request method of the CXML Webhook. |
| `status_callback_url` | body | `string` | no | Status callback url of the CXML Webhook. |
| `status_callback_method` | body | `string` | no | Status callback method of the CXML Webhook. |
