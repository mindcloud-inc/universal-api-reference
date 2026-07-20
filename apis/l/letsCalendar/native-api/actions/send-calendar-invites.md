# Send Calendar Invites with Let's Calendar

Sends calendar invites to attendees in Let's Calendar.

## Endpoint

- **Method:** `POST`
- **Path:** `send-invite`
- **Base URL:** `https://panel.letscalendar.com/api/lc`
- **Official documentation:** [Send Calendar Invites](https://panel.letscalendar.com/docs#apis-POSTapi-lc-send-invite)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `string` | yes | The unique identifier of the campaign. |
