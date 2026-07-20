# Get Channel Info with Pushbullet

Finds channel details in Pushbullet by channel tag.

## Endpoint

- **Method:** `GET`
- **Path:** `/channel-info`
- **Base URL:** `https://api.pushbullet.com/v2`
- **Official documentation:** [Get Channel Info](https://docs.pushbullet.com/v8/#subscriptions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | query | `string` | yes | Channel tag to look up. |
