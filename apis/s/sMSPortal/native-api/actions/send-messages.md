# Send Messages with SMSPortal

## Endpoint

- **Method:** `POST`
- **Path:** `/BulkMessages`
- **Base URL:** `https://rest.smsportal.com/v3`
- **Official documentation:** [Send Messages](https://docs.smsportal.com/reference/bulkmessages_postv3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Messages[]` | body | `array<object>` | yes | One or more SMS messages to send. |
| `sendOptions.testMode` | body | `boolean` | no | — |
| `Messages[].Content` | body | `string` | yes | The SMS message text to send. |
| `sendOptions` | body | `object` | no | — |
| `Messages[].Destination` | body | `string` | yes | The destination mobile number in international format. |
