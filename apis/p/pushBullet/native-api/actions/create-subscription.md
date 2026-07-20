# Create Subscription with Pushbullet

Creates a new subscription in Pushbullet.

## Endpoint

- **Method:** `POST`
- **Path:** `/subscriptions`
- **Base URL:** `https://api.pushbullet.com/v2`
- **Official documentation:** [Create Subscription](https://docs.pushbullet.com/v8/#subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_tag` | body | `string` | yes | Channel tag to subscribe to. |
