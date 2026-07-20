# Add Person with Pipedrive

Creates a new person in Pipedrive.

## Endpoint

- **Method:** `POST`
- **Path:** `v2/persons`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Add Person](https://developers.pipedrive.com/docs/api/v1/Persons#addPerson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Full name of the person. |
| `owner_id` | body | `number` | no | Owner user ID for the person. |
| `org_id` | body | `number` | no | Organization ID linked to the person. |
| `label_ids` | body | `list<number>` | no | Label IDs to assign to the person. |
| `emails` | body | `list<object>` | no | Array of email objects for the person. |
| `phones` | body | `list<object>` | no | Array of phone objects for the person. |
| `visible_to` | body | `string` | no | Visibility setting for the person record. |
