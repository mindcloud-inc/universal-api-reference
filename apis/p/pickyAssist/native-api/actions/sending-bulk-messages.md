# Sending Bulk Messages with Picky Assist

## Endpoint

- **Method:** `POST`
- **Path:** `/push`
- **Base URL:** `https://app.pickyassist.com/api/v2`
- **Official documentation:** [Sending Bulk Messages](https://help.pickyassist.com/api-documentation-v2/push-api/sending-bulk-messages-push)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `priority` | body | `string` | no | Message priority value used by Picky Assist. |
| `application` | body | `string` | yes | The channel/application id that should send the message. |
| `globalmessage` | body | `string` | yes | Shared message text used for all recipient rows in the bulk request. |
| `data[]` | body | `array<object>` | yes | Recipient rows for the bulk push request. |
