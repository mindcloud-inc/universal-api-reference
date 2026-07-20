# Delete Device with Pushbullet

Deletes an existing device from Pushbullet.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/devices/:device_iden`
- **Base URL:** `https://api.pushbullet.com/v2`
- **Official documentation:** [Delete Device](https://docs.pushbullet.com/v8/#devices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_iden` | path | `string` | yes | Device identifier to delete. |
