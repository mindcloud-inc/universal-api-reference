# Update Person with Pipedrive

Updates an existing person in Pipedrive.

## Endpoint

- **Method:** `PATCH`
- **Path:** `v2/persons/:id`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Update Person](https://developers.pipedrive.com/docs/api/v1/Persons#updatePerson)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique ID of the person to update. |
| `name` | body | `string` | no | Updated full name of the person. |
| `owner_id` | body | `number` | no | Updated owner user ID. |
| `org_id` | body | `number` | no | Updated organization ID. |
| `label_ids` | body | `list<number>` | no | Updated label IDs for the person. |
| `emails` | body | `list<object>` | no | Updated email array for the person. |
| `phones` | body | `list<object>` | no | Updated phone array for the person. |
| `visible_to` | body | `string` | no | Updated visibility setting. |
