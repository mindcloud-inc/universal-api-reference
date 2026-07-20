# Send Message with Brosix

Creates a new message in Brosix for a user or chat room.

## Endpoint

- **Method:** `POST`
- **Path:** `/message/send/`
- **Base URL:** `https://box-n2.brosix.com/api/v1`
- **Official documentation:** [Send Message](https://help.brosix.com/notifications-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `msg` | query | `string` | yes | The text to send to the configured Brosix channel. |
