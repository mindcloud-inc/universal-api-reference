# Create A New Author with Moderation API

Creates a new author in Moderation API.

## Endpoint

- **Method:** `POST`
- **Path:** `/authors`
- **Base URL:** `https://api.moderationapi.com/v1`
- **Official documentation:** [Create A New Author](https://docs.moderationapi.com/api-reference/author/create-a-new-author)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile_picture` | body | `string` | no | URL of the author's profile picture |
| `external_link` | body | `string` | no | URL of the author's external profile |
| `name` | body | `string` | no | Author name or identifier |
| `email` | body | `string` | no | Author email address |
| `company` | body | `string` | no | The author's company or organization |
| `metadata` | body | `object` | no | Additional metadata provided by your system. We recommend including any relevant information that may assist in the moderation process. |
| `first_seen` | body | `number` | no | Timestamp when author first appeared |
| `last_seen` | body | `number` | no | Timestamp of last activity |
| `manual_trust_level` | body | `number` | no | — |
| `external_id` | body | `string` | yes | External ID of the user, typically the ID of the author in your database. |
