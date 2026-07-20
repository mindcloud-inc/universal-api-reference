# Track Event with Product Fruits

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/events/track`
- **Base URL:** `https://api.productfruits.com`
- **Official documentation:** [Track Event](https://help.productfruits.com/en/article/events-tracking)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | Name of the event to track. |
| `properties.username` | body | `string` | yes | Username of the user to track the event to. |
