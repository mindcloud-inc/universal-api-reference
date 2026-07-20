# Trigger BippyBox with BippyBox

Triggers a BippyBox device with audio and color.

## Endpoint

- **Method:** `POST`
- **Path:** `https://mqtt.bippybox.io/send`
- **Base URL:** `https://app.bippybox.io`
- **Official documentation:** [Trigger BippyBox](https://bippybox.io/docs/#apikey)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | body | `string` | yes | Your BippyBox UID used to authenticate the request. |
| `deviceID` | body | `string` | yes | The ID of the synced BippyBox device to trigger. |
| `URL` | body | `string` | yes | A hosted OGG audio file URL to play on the BippyBox. |
| `color` | body | `string` | yes | Hex color for the trigger effect. |
