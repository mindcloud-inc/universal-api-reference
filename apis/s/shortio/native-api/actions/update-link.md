# Update Link with Short.io

Updates an existing link in Short.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/links/:linkId`
- **Base URL:** `https://api.short.io`
- **Official documentation:** [Update Link](https://developers.short.io/reference/post_links-linkid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `linkId` | path | `string` | yes | Link ID. |
| `originalURL` | body | `string` | no | Original URL. |
| `path` | body | `string` | no | Link slug. |
| `title` | body | `string` | no | Link title. |
| `tags[]` | body | `array<string>` | no | Array of link tags. |
| `domainId` | query | `string` | no | Domain ID. |
| `ttl` | body | `string` | no | Time to live in milliseconds or ISO string. |
| `expiresAt` | body | `string` | no | Link expiration date in milliseconds or ISO string. |
| `redirectType` | body | `number` | no | HTTP redirect code. |
| `password` | body | `string` | no | Link password. |
| `cloaking` | body | `boolean` | no | Enable cloaking. |
| `clicksLimit` | body | `number` | no | Disable the link after this number of clicks. |
| `passwordContact` | body | `boolean` | no | Provide your email to users to get a password. |
| `skipQS` | body | `boolean` | no | Skip query string merging. |
| `archived` | body | `boolean` | no | Archive the link. |
| `expiredURL` | body | `string` | no | URL to use after expiration. |
| `utmSource` | body | `string` | no | Set the utm_source parameter. |
| `utmMedium` | body | `string` | no | Set the utm_medium parameter. |
| `utmCampaign` | body | `string` | no | Set the utm_campaign parameter. |
| `utmTerm` | body | `string` | no | Set the utm_term parameter. |
| `utmContent` | body | `string` | no | Set the utm_content parameter. |
