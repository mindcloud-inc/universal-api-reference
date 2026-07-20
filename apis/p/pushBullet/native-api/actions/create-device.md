# Create Device with Pushbullet

Creates a new device in Pushbullet.

## Endpoint

- **Method:** `POST`
- **Path:** `/devices`
- **Base URL:** `https://api.pushbullet.com/v2`
- **Official documentation:** [Create Device](https://docs.pushbullet.com/v8/#devices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `nickname` | body | `string` | yes | Nickname for the device. |
| `type` | body | `string` | yes | Device type (for example stream). |
