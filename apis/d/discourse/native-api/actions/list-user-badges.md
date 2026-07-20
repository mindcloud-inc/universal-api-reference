# List User Badges with Discourse

Retrieves badges for a Discourse user.

## Endpoint

- **Method:** `GET`
- **Path:** `/user-badges/:username.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [List User Badges](https://docs.discourse.org/#tag/Badges/operation/listUserBadges)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | path | `string` | yes | Discourse username. |
