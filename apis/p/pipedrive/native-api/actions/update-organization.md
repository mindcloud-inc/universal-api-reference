# Update Organization with Pipedrive

Updates an existing organization in Pipedrive.

## Endpoint

- **Method:** `PATCH`
- **Path:** `v2/organizations/:id`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Update Organization](https://developers.pipedrive.com/docs/api/v1/Organizations#updateOrganization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Unique ID of the organization to update. |
| `name` | body | `string` | no | Updated organization name. |
| `owner_id` | body | `number` | no | Updated owner user ID. |
| `address` | body | `object` | no | Updated address object for the organization. |
| `label_ids` | body | `list<number>` | no | Updated label IDs for the organization. |
| `visible_to` | body | `string` | no | Updated visibility setting. |
