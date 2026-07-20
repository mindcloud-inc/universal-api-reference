# Update SWML Webhook with SignalWire

Updates an existing SWML webhook in SignalWire.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/fabric/resources/swml_webhooks/{id}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Update SWML Webhook](https://signalwire.com/docs/apis/rest/swml-webhook/update-swml-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of a SWML Webhook. |
| `name` | body | `string` | no | Name of the SWML Webhook. |
| `used_for` | body | `string` | no | Used for of the SWML Webhook. |
| `primary_request_url` | body | `string` | no | Primary request url of the SWML Webhook. |
| `primary_request_method` | body | `string` | no | Primary request method of the SWML Webhook. |
| `fallback_request_url` | body | `string` | no | Fallback request url of the SWML Webhook. |
| `fallback_request_method` | body | `string` | no | Fallback request method of the SWML Webhook. |
| `status_callback_url` | body | `string` | no | Status callback url of the SWML Webhook. |
| `status_callback_method` | body | `string` | no | Status callback method of the SWML Webhook. |
