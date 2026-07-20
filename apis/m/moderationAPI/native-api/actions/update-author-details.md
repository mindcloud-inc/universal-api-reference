# Update Author Details with Moderation API

Updates author details in Moderation API.

## Endpoint

- **Method:** `PUT`
- **Path:** `/authors/:id`
- **Base URL:** `https://api.moderationapi.com/v1`
- **Official documentation:** [Update Author Details](https://docs.moderationapi.com/api-reference/author/update-author-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Either external ID or the ID assigned by moderation API. |
| `profile_picture` | body | `string` | no | URL of the author's profile picture |
| `external_link` | body | `string` | no | URL of the author's external profile |
| `name` | body | `string` | no | Author name or identifier |
| `email` | body | `string` | no | Author email address |
| `company` | body | `string` | no | The author's company or organization |
| `metadata` | body | `object` | no | Additional metadata provided by your system. We recommend including any relevant information that may assist in the moderation process. |
| `first_seen` | body | `number` | no | Timestamp when author first appeared |
| `last_seen` | body | `number` | no | Timestamp of last activity |
| `manual_trust_level` | body | `number` | no | — |
