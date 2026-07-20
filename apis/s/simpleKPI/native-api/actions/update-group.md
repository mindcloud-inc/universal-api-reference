# Update Group with SimpleKPI

Updates an existing group in SimpleKPI.

## Endpoint

- **Method:** `PUT`
- **Path:** `groups/:id`
- **Base URL:** `https://{subdomain}.simplekpi.com/api/`
- **Official documentation:** [Update Group](https://support.simplekpi.com/Developers/Groups)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | no | The group ID. |
| `name` | body | `string` | no | The group name. |
| `sort_order` | body | `number` | no | The display sort order for the group. |
