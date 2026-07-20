# Track Event with SatisMeter

## Endpoint

- **Method:** `POST`
- **Path:** `/api/users`
- **Base URL:** `https://app.satismeter.com`
- **Official documentation:** [Track Event](https://support.satismeter.com/hc/en-us/articles/6980481518227-Track-event-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | Event name. |
| `project` | body | `string` | yes | Project ID. |
| `userId` | body | `string` | yes | User ID used on your end to uniquely identify the user. |
