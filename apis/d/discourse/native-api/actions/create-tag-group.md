# Create Tag Group with Discourse

Creates a new tag group in Discourse.

## Endpoint

- **Method:** `POST`
- **Path:** `/tag_groups.json`
- **Base URL:** `https://mindcloud.discourse.group`
- **Official documentation:** [Create Tag Group](https://docs.discourse.org/#tag/Tags/operation/createTagGroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Tag group name. |
