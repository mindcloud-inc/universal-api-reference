# Add User To Group with Easy Redmine

Adds a user to a group in Easy Redmine.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/:id/users.json`
- **Base URL:** `https://3f73561b8b.bigus-e5.easy8.com`
- **Official documentation:** [Add User To Group](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the group to add users to. |
| `user_ids[]` | body | `array<number>` | yes | IDs of users to add to the group. |
