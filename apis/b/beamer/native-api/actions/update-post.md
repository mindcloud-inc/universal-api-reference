# Update Post with Beamer

Updates an existing post in Beamer.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v0/posts/:postId`
- **Base URL:** `https://api.getbeamer.com`
- **Official documentation:** [Update Post](https://help.userflow.com/beamer/docs/beamer-api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `postId` | path | `number` | yes | — |
| `title[]` | body | `array<string>` | yes | Send multiple values as a array. |
| `content[]` | body | `array<string>` | yes | Send multiple values as a array. |
| `category` | body | `string` | yes | — |
| `publish` | body | `boolean` | no | — |
| `archive` | body | `boolean` | no | — |
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
| `userEmail` | body | `string` | no | — |
| `fixedBoostedAnnouncement` | body | `boolean` | no | — |
