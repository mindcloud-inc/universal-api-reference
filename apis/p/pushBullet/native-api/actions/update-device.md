# Update Device with Pushbullet

Updates an existing device in Pushbullet.

## Endpoint

- **Method:** `POST`
- **Path:** `/devices/:device_iden`
- **Base URL:** `https://api.pushbullet.com/v2`
- **Official documentation:** [Update Device](https://docs.pushbullet.com/v8/#devices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_iden` | path | `string` | yes | Device identifier to update. |
| `nickname` | body | `string` | yes | Updated nickname for the device. |
