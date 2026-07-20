# Remove Issue Watcher with Easy Redmine

Removes a watcher from an issue in Easy Redmine.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/issues/:id/watchers/:userId.json`
- **Base URL:** `https://3f73561b8b.bigus-e5.easy8.com`
- **Official documentation:** [Remove Issue Watcher](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the issue to remove a watcher from. |
| `user_id` | path | `number` | yes | ID of the watcher user to remove. |
