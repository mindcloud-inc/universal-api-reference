# Create List with Emailchef

Creates a new mailing list in Emailchef.

## Endpoint

- **Method:** `POST`
- **Path:** `lists`
- **Base URL:** `https://app.emailchef.com/apps/api/v1`
- **Official documentation:** [Create List](https://emailchef.com/integration/#/Lists/createList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `instance_in.list_name` | body | `string` | yes | The name of the list to create. |
| `instance_in.list_description` | body | `string` | no | Optional description for the list. |
