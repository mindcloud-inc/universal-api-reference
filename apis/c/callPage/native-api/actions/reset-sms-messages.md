# Reset SMS Messages with CallPage

Deletes all SMS messages from CallPage.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/reset`
- **Base URL:** `https://core.callpage.io/api/v1/external`
- **Official documentation:** [Reset SMS Messages](https://callpage.github.io/documentation-rest/#reset-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `widget_id` | body | `number` | yes | The widget identifier. |
| `message_id` | body | `list<string>` | no | The SMS message identifier. Accepted values: `visitor.call-scheduled`, `visitor.cancel-scheduled`, `visitor.dial-completed`, `visitor.incoming-dial-completed`. |
