# Create Post with Beamer

Creates a new post in Beamer.

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/posts`
- **Base URL:** `https://api.getbeamer.com`
- **Official documentation:** [Create Post](https://help.userflow.com/beamer/docs/beamer-api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title[]` | body | `array<string>` | yes | Title of the post. Send multiple values as a array. |
| `content[]` | body | `array<string>` | yes | Content of the post. Send multiple values as a array. |
| `category` | body | `string` | yes | Category for the post. |
| `publish` | body | `boolean` | no | Whether to publish the post or save it as a draft. |
| `archive` | body | `boolean` | no | Whether to archive the post. |
| `pinned` | body | `boolean` | no | — |
| `showInWidget` | body | `boolean` | no | — |
| `showInStandalone` | body | `boolean` | no | — |
| `boostedAnnouncement` | body | `string` | no | — |
| `linkUrl[]` | body | `array<string>` | no | Send multiple values as a array. |
| `linkText[]` | body | `array<string>` | no | Send multiple values as a array. |
| `linksInNewWindow` | body | `boolean` | no | — |
| `date` | body | `string` | no | — |
| `dueDate` | body | `string` | no | — |
| `language[]` | body | `array<string>` | no | Send multiple values as a array. |
| `filter` | body | `string` | no | — |
| `filterUserId` | body | `string` | no | — |
| `filterUrl` | body | `string` | no | — |
| `enableFeedback` | body | `boolean` | no | — |
| `enableReactions` | body | `boolean` | no | — |
| `enableSocialShare` | body | `boolean` | no | — |
| `autoOpen` | body | `boolean` | no | — |
| `sendPushNotification` | body | `boolean` | no | — |
| `userEmail` | body | `string` | no | Email of the user in your account creating this post. |
| `fixedBoostedAnnouncement` | body | `boolean` | no | — |
