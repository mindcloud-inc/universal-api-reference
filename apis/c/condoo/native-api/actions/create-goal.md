# Create Goal with condoo

Creates a new goal in condoo.

## Endpoint

- **Method:** `POST`
- **Path:** `/goals`
- **Base URL:** `https://trk.condoo.systems/api`
- **Official documentation:** [Create Goal](https://trk.condoo.systems/en/api-documentation/goals)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | no | Optional custom goal key. |
| `name` | body | `string` | yes | Required goal name. |
| `path` | body | `string` | no | Optional path when type is pageview. |
| `type` | body | `string` | yes | Required goal type. Allowed values: pageview, custom. |
| `website_id` | body | `number` | yes | Required website ID. |
