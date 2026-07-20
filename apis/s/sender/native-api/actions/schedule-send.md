# Schedule Send with Sender

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:id/schedule`
- **Base URL:** `https://api.sender.net/v2`
- **Official documentation:** [Schedule Send](https://api.sender.net/campaigns/schedule-send/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Campaign ID. |
| `schedule_time` | body | `date` | yes | Send date and time in Y-m-d H:i:s format. |
