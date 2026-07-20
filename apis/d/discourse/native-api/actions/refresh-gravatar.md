# Refresh Gravatar with Discourse

Refreshes the Gravatar for a Discourse user.

## Endpoint

- **Method:** `POST`
- **Path:** `/user_avatar/:username/refresh_gravatar.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Refresh Gravatar](https://docs.discourse.org/#tag/Users/operation/refreshGravatar)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Username. |
