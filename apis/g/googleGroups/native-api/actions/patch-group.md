# Patch Group with Google Groups

Updates an existing group in Google Groups.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://admin.googleapis.com/admin/directory/v1/groups/:groupKey`
- **Base URL:** `https://groups.google.com`
- **Official documentation:** [Patch Group](https://developers.google.com/admin-sdk/directory/reference/rest/v1/groups/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupKey` | path | `string` | yes | The group email address, group alias, or unique group ID. |
| `email` | body | `string` | no | The group's primary email address. |
| `name` | body | `string` | no | The group's display name. |
| `description` | body | `string` | no | An optional description for the group. |
