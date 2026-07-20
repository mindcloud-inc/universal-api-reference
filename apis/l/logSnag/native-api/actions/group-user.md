# Group User with LogSnag

## Endpoint

- **Method:** `POST`
- **Path:** `/group`
- **Base URL:** `https://api.logsnag.com/v1`
- **Official documentation:** [Group User](https://docs.logsnag.com/sdks/node)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `string` | yes | Project name in LogSnag. |
| `group_id` | body | `string` | yes | Group identifier to associate or update. |
| `user_id` | body | `string` | yes | User identifier to associate with the group. |
| `properties` | body | `object` | no | Optional group properties as key/value pairs. |
