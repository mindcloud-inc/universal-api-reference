# Create Link with Short.io

Creates a new link in Short.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/links`
- **Base URL:** `https://api.short.io`
- **Official documentation:** [Create Link](https://developers.short.io/reference/post_links)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `originalURL` | body | `string` | yes | Original URL. |
| `domain` | body | `string` | yes | Domain hostname. |
| `path` | body | `string` | no | Custom link slug. |
| `title` | body | `string` | no | Link title. |
| `tags[]` | body | `array<string>` | no | Array of link tags. |
| `allowDuplicates` | body | `boolean` | no | Allow creating duplicate links for the same original URL. |
| `folderId` | body | `string` | no | Folder ID. |
| `ttl` | body | `string` | no | Time to live in milliseconds or ISO string. |
| `expiresAt` | body | `string` | no | Link expiration date in milliseconds or ISO string. |
| `redirectType` | body | `number` | no | HTTP redirect code. |
| `password` | body | `string` | no | Link password. |
| `cloaking` | body | `boolean` | no | Enable cloaking. |
| `clicksLimit` | body | `number` | no | Disable the link after this number of clicks. |
| `passwordContact` | body | `boolean` | no | Provide your email to users to get a password. |
| `skipQS` | body | `boolean` | no | Skip query string merging. |
| `archived` | body | `boolean` | no | Archive the link on creation. |
| `expiredURL` | body | `string` | no | URL to use after expiration. |
| `utmSource` | body | `string` | no | Set the utm_source parameter. |
| `utmMedium` | body | `string` | no | Set the utm_medium parameter. |
| `utmCampaign` | body | `string` | no | Set the utm_campaign parameter. |
| `utmTerm` | body | `string` | no | Set the utm_term parameter. |
| `utmContent` | body | `string` | no | Set the utm_content parameter. |
