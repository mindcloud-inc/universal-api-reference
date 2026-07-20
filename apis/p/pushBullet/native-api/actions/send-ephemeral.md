# Send Ephemeral with Pushbullet

Sends an ephemeral message to the Pushbullet realtime stream.

## Endpoint

- **Method:** `POST`
- **Path:** `/ephemerals`
- **Base URL:** `https://api.pushbullet.com/v2`
- **Official documentation:** [Send Ephemeral](https://docs.pushbullet.com/v8/#ephemerals)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Ephemeral payload type. |
| `push` | body | `object` | no | Nested push payload for ephemeral type=push. |
