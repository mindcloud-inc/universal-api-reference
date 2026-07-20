# Update Group with Zubie

Updates an existing group in Zubie.

## Endpoint

- **Method:** `POST`
- **Path:** `/group/{group_key}`
- **Base URL:** `https://api.zubiecar.com/api/v2/zinc`
- **Official documentation:** [Update Group](https://developer.zubie.com/reference/groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_key` | path | `string` | yes | Unique group key. |
| `name` | body | `string` | yes | Group name. |
