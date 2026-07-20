# Create a scheduled message with xMatters

Creates a scheduled message in your xMatters instance.

## Endpoint

- **Method:** `POST`
- **Path:** `scheduled-messages`
- **Base URL:** `https://mindcloud.xmatters.com/api/xm/1`
- **Official documentation:** [Create a scheduled message](https://help.xmatters.com/xmapi/index.html#create-a-scheduled-message)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `event` | body | `string` | no |
| `name` | body | `string` | no |
| `recurrence` | body | `string` | no |
