# Create a new configuration in a particular group with Qase

Creates a new configuration in a Qase group.

## Endpoint

- **Method:** `POST`
- **Path:** `/configuration/:code`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Create a new configuration in a particular group](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | path | `string` | yes | Code of project, where to search entities. |
| `title` | body | `string` | yes | Required request field title. |
| `group_id` | body | `number` | yes | Required request field group_id. |
