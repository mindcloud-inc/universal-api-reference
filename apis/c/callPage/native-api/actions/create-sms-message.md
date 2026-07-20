# Create SMS Message with CallPage

Creates a new SMS message in CallPage.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/create`
- **Base URL:** `https://core.callpage.io/api/v1/external`
- **Official documentation:** [Create SMS Message](https://callpage.github.io/documentation-rest/#create-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `widget_id` | body | `number` | yes | The widget identifier. |
| `message_id` | body | `list<string>` | yes | The SMS message identifier. Accepted values: `visitor.call-scheduled`, `visitor.cancel-scheduled`, `visitor.dial-completed`, `visitor.incoming-dial-completed`. |
| `enabled` | body | `boolean` | no | Whether the SMS should be enabled. |
| `text` | body | `string` | yes | The SMS text. Maximum 240 characters. |
