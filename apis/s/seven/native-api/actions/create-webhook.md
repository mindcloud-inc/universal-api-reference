# Create Webhook with Seven

Creates a new webhook in Seven.

## Endpoint

- **Method:** `POST`
- **Path:** `/hooks`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Create Webhook](https://docs.seven.io/en/rest-api/endpoints/webhooks#register-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `target_url` | body | `string` | yes | Destination address of your webhook |
| `headers` | body | `string` | no | Custom headers to be sent to the webhook URL. Could contain multiple headers separated by a line break. |
| `event_type` | body | `string` | yes | Type of event for which you would like to receive a webhook.  Show events all - Sends all events  rcs - RCS events and inbound RCS messages  sms_mo - New inbound SMS  dlr - Status reports of your SMS  voice_call - Info about voice calls  voice_status - Status updates of voice calls  voice_dtmf - Incoming DTMF signals in voice calls  tracking - Clicks or views of the Performance Tracking |
| `event_filter` | body | `string` | no | Optional. Sends the webhook only if the filter applies. For example, for different webhooks with different inbound numbers. |
| `request_method` | body | `string` | no | Request method in which you would like to receive the webhook.  POST - Data is sent as an HTTP POST request as application/x-www-form-urlencoded (default)  GET - Data is sent as HTTP GET parameter  JSON - Data is sent via HTTP POST as JSON payload |
