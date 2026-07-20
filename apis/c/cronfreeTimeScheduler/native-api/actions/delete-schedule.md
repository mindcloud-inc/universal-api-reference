# Delete Schedule with Cronfree Time Scheduler

Deletes an existing schedule from Cronfree Time Scheduler.

## Endpoint

- **Method:** `POST`
- **Path:** `/unschedule`
- **Base URL:** `https://login.cronfree.com/zapier`
- **Official documentation:** [Delete Schedule](https://docs.cronfree.com/api#unsubscribe)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hookUrl` | body | `string` | yes | The scheduled webhook URL to remove from Cronfree. |
