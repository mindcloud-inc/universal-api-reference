# Update Group with HelpDocs

Updates an existing group in HelpDocs.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/account/group/:group_id`
- **Base URL:** `https://api.helpdocs.io/v1`
- **Official documentation:** [Update Group](https://apidocs.helpdocs.io/article/r5k7g79ici-updating-a-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `group_id` | path | `string` | yes | Group ID to update. |
| `name` | body | `string` | no | Updated group name. |
