# Create SWML Webhook with SignalWire

Creates a new SWML webhook in SignalWire.

## Endpoint

- **Method:** `POST`
- **Path:** `/fabric/resources/swml_webhooks`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Create SWML Webhook](https://signalwire.com/docs/apis/rest/swml-webhook/create-swml-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Name of the SWML Webhook. |
| `used_for` | body | `string` | no | Used for of the SWML Webhook. |
| `primary_request_url` | body | `string` | yes | Primary request url of the SWML Webhook. |
| `primary_request_method` | body | `string` | no | Primary request method of the SWML Webhook. |
| `fallback_request_url` | body | `string` | no | Fallback request url of the SWML Webhook. |
| `fallback_request_method` | body | `string` | no | Fallback request method of the SWML Webhook. |
| `status_callback_url` | body | `string` | no | Status callback url of the SWML Webhook. |
| `status_callback_method` | body | `string` | no | Status callback method of the SWML Webhook. |
