# Sending Dynamic Messages with Picky Assist

## Endpoint

- **Method:** `POST`
- **Path:** `/push`
- **Base URL:** `https://app.pickyassist.com/api/v2`
- **Official documentation:** [Sending Dynamic Messages](https://help.pickyassist.com/api-documentation-v2/push-api/sending-dynamic-messages-push)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `priority` | body | `string` | no | Message priority value used by Picky Assist. |
| `application` | body | `string` | yes | The channel/application id that should send the message. |
| `data[]` | body | `array<object>` | yes | Recipient rows and message variables for the dynamic push request. |
