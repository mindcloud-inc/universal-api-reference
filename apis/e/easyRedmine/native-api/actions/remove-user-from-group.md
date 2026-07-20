# Remove User From Group with Easy Redmine

Removes a user from a group in Easy Redmine.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/groups/:id/users/:userId.json`
- **Base URL:** `https://3f73561b8b.bigus-e5.easy8.com`
- **Official documentation:** [Remove User From Group](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the group to remove a user from. |
| `user_id` | path | `number` | yes | ID of the user to remove from the group. |
