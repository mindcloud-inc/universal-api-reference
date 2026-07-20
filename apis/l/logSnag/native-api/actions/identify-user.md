# Identify User with LogSnag

## Endpoint

- **Method:** `POST`
- **Path:** `/identify`
- **Base URL:** `https://api.logsnag.com/v1`
- **Official documentation:** [Identify User](https://docs.logsnag.com/api-reference/identify)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `string` | yes | Project name in LogSnag. |
| `user_id` | body | `string` | yes | User ID to identify. |
| `properties` | body | `object` | yes | User properties as key/value pairs. |
