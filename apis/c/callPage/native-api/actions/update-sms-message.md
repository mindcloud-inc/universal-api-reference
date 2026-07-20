# Update SMS Message with CallPage

Updates an existing SMS message in CallPage.

## Endpoint

- **Method:** `POST`
- **Path:** `/sms/update`
- **Base URL:** `https://core.callpage.io/api/v1/external`
- **Official documentation:** [Update SMS Message](https://callpage.github.io/documentation-rest/#update-sms)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `widget_id` | body | `number` | yes | The widget identifier. |
| `message_id` | body | `list<string>` | yes | The SMS message identifier. Accepted values: `visitor.call-scheduled`, `visitor.cancel-scheduled`, `visitor.dial-completed`, `visitor.incoming-dial-completed`. |
| `enabled` | body | `boolean` | no | Whether the SMS should be enabled. |
| `text` | body | `string` | yes | The SMS text. Maximum 240 characters. |
