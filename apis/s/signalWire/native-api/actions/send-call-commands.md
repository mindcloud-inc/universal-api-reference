# Send Call Commands with SignalWire

Sends call commands to SignalWire calls.

## Endpoint

- **Method:** `POST`
- **Path:** `/calling/calls`
- **Base URL:** `https://mindcloud.signalwire.com/api`
- **Official documentation:** [Send Call Commands](https://signalwire.com/docs/apis/rest/calls/call-commands)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `command` | body | `string` | yes | The `dial` command is used to create a new call. |
| `params.from` | body | `string` | yes | The address that initiated the call. Can be either a E.164 formatted number (`+xxxxxxxxxxx`), or a SIP endpoint (`sip:xxx@yyy.zzz`). |
| `params.to` | body | `string` | yes | The address that received the call. Can be either a E.164 formatted number (`+xxxxxxxxxxx`), or a SIP endpoint (`sip:xxx@yyy.zzz`). |
| `params.caller_id` | body | `string` | no | The number, in E.164 format, or identifier of the caller. |
| `params.fallback_url` | body | `string` | no | The Fallback URL to handle the call. This parameter allows you to specify a backup webhook or different route in your code containing SWML instructions for handling the call. |
| `params.status_url` | body | `string` | no | A URL that will recieve status updates of the current call. Any call events defined in `status_events` will be delivered to the defined URL. |
| `params.status_events[]` | body | `array<string>` | no | The call events that will be monitored and sent to the `status_url` when active. |
| `params.url` | body | `string` | yes | The URL to handle the call. This parameter allows you to specify a webhook or different route in your code containing SWML instructions for handling the call. Either `url` or `swml` must be included for a new call. |
