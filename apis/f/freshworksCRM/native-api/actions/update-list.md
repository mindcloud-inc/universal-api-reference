# Update List with Freshworks CRM

Updates an existing list in Freshworks CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/lists/:id`
- **Base URL:** `https://{bundleAlias}`
- **Official documentation:** [Update List](https://developers.freshworks.com/crm/api/#update_a_list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `name` | body | `string` | no | List name |
