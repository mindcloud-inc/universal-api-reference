# Create Group with Google Groups

Creates a new group in Google Groups.

## Endpoint

- **Method:** `POST`
- **Path:** `https://admin.googleapis.com/admin/directory/v1/groups`
- **Base URL:** `https://groups.google.com`
- **Official documentation:** [Create Group](https://developers.google.com/admin-sdk/directory/reference/rest/v1/groups/insert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The group's primary email address. This field is required when creating a group. |
| `name` | body | `string` | no | The group's display name. |
| `description` | body | `string` | no | An optional description for the group. |
