# Update Tag Group with Discourse

Updates an existing tag group in Discourse.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tag_groups/:id.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Update Tag Group](https://docs.discourse.org/#tag/Tags/operation/updateTagGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Tag group id. |
| `one_per_topic` | body | `boolean` | no | Whether only one tag from the group can be used per topic. |
| `parent_tag_name` | body | `string` | no | Optional parent tag name for the group. |
| `permissions` | body | `string` | no | Optional tag group permissions map. |
| `tag_names` | body | `string` | no | List of tags that belong to the tag group. |
| `name` | body | `string` | yes | Updated name for the Discourse tag group. |
