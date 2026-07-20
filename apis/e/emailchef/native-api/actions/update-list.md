# Update List with Emailchef

Updates an existing mailing list in Emailchef.

## Endpoint

- **Method:** `PUT`
- **Path:** `lists/:list_id`
- **Base URL:** `https://app.emailchef.com/apps/api/v1`
- **Official documentation:** [Update List](https://emailchef.com/integration/#/Lists/updateList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | The Emailchef list ID. |
| `instance_in.list_name` | body | `string` | no | The updated name for the list. |
| `instance_in.list_description` | body | `string` | no | The updated description for the list. |
