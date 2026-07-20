# Toggle Campaign Automation Status with Let's Calendar

Updates campaign automation status in Let's Calendar.

## Endpoint

- **Method:** `POST`
- **Path:** `toggle-automation`
- **Base URL:** `https://panel.letscalendar.com/api/lc`
- **Official documentation:** [Toggle Campaign Automation Status](https://panel.letscalendar.com/docs#apis-POSTapi-lc-toggle-automation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `string` | yes | The unique identifier of the campaign. |
| `enabled` | body | `boolean` | yes | Set to true to enable automation, false to disable it. |
