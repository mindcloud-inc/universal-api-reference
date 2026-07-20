# Send Notification with Hook.Notifier

Sends a custom notification through Hook.Notifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://hooknotifier.com/{identifier}/{apiKey}`
- **Official documentation:** [Send Notification](https://hooknotifier.com/blog/get-started-with-hook-notifier)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `object` | query | `string` | yes | Title of the notification. |
| `body` | query | `string` | yes | Content of the notification. |
| `tags` | query | `string` | no | Comma-separated tags for filtering, for example general,ops. |
| `color` | query | `string` | no | Hex color for the notification, for example #FFC107. |
| `redirectUrl` | query | `string` | no | URL opened when the notification is clicked. Premium feature. |
| `image` | query | `string` | no | Image URL shown inside the notification. |
| `sendToTeam` | query | `boolean` | no | Send the notification to you and your team. Premium feature. |
| `sound` | query | `boolean` | no | Activate the notification sound on phone. |
| `preventData` | query | `boolean` | no | Disable data storage in the notification. |
