# Add Organization with Pipedrive

Creates a new organization in Pipedrive.

## Endpoint

- **Method:** `POST`
- **Path:** `v2/organizations`
- **Base URL:** `{api_domain}/api`
- **Official documentation:** [Add Organization](https://developers.pipedrive.com/docs/api/v1/Organizations#addOrganization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the organization. |
| `owner_id` | body | `number` | no | Owner user ID for the organization. |
| `address` | body | `object` | no | Address object for the organization. |
| `label_ids` | body | `list<number>` | no | Label IDs to assign to the organization. |
| `visible_to` | body | `string` | no | Visibility setting for the organization record. |
