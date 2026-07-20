# Update cXML Application with SignalWire

Updates an existing cXML application in SignalWire.

## Endpoint

- **Method:** `PUT`
- **Path:** `/fabric/resources/cxml_applications/{id}`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Update cXML Application](https://signalwire.com/docs/apis/rest/cxml-applications/update-cxml-application)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique ID of a cXML Application. |
| `display_name` | body | `string` | no | Display name of the cXML Application |
| `account_sid` | body | `string` | no | Project ID for the cXML Application |
| `voice_url` | body | `string` | no | URL to handle incoming calls |
| `voice_method` | body | `string` | no | HTTP method for voice URL |
| `voice_fallback_url` | body | `string` | no | Fallback URL for voice errors |
| `voice_fallback_method` | body | `string` | no | HTTP method for voice fallback URL |
| `status_callback` | body | `string` | no | URL to receive status callbacks |
| `status_callback_method` | body | `string` | no | HTTP method for status callbacks |
| `sms_url` | body | `string` | no | URL to handle incoming messages |
| `sms_method` | body | `string` | no | HTTP method for SMS URL |
| `sms_fallback_url` | body | `string` | no | Fallback URL for SMS errors |
| `sms_fallback_method` | body | `string` | no | HTTP method for SMS fallback URL |
| `sms_status_callback` | body | `string` | no | URL to receive SMS status callbacks |
| `sms_status_callback_method` | body | `string` | no | HTTP method for SMS status callbacks |
