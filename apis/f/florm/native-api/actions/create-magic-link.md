# Create Magic Link with Florm

Creates a login magic link in Florm.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/auth/magic-links`
- **Base URL:** `https://api.florm.io`
- **Official documentation:** [Create Magic Link](https://api.florm.io/docs#/default/create_magic_link_v1_auth_magic_links_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to receive the Florm magic link. |
