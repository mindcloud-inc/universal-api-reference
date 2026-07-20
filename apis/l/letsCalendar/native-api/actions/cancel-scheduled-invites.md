# Cancel Scheduled Invites with Let's Calendar

Cancels scheduled invites in Let's Calendar.

## Endpoint

- **Method:** `POST`
- **Path:** `cancel-scheduled-invite`
- **Base URL:** `https://panel.letscalendar.com/api/lc`
- **Official documentation:** [Cancel Scheduled Invites](https://panel.letscalendar.com/docs#apis-POSTapi-lc-cancel-scheduled-invite)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `string` | yes | The unique identifier of the campaign. |
