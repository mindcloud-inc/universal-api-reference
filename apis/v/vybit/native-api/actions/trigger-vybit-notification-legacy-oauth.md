# Trigger Vybit Notification (Legacy OAuth) with Vybit

## Endpoint

- **Method:** `POST`
- **Path:** `/fire/{{triggerKey}}`
- **Base URL:** `https://api.vybit.net/v1`
- **Official documentation:** [Trigger Vybit Notification (Legacy OAuth)](https://developer.vybit.net/oauth-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `imageUrl` | body | `string` | no | Optional image URL to attach to the notification. |
| `linkUrl` | body | `string` | no | Optional redirect URL when the notification is tapped. |
| `log` | body | `string` | no | Optional content to append to the Vybit log. |
| `message` | body | `string` | no | Optional message to display with the notification. |
| `triggerKey` | path | `string` | yes | The legacy trigger key of the vybit to fire. |
