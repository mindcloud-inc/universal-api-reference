# Add Issue Watcher with Easy Redmine

Adds a watcher to an issue in Easy Redmine.

## Endpoint

- **Method:** `POST`
- **Path:** `/issues/:id/watchers.json`
- **Base URL:** `https://3f73561b8b.bigus-e5.easy8.com`
- **Official documentation:** [Add Issue Watcher](https://3f73561b8b.bigus-e5.easy8.com/easy_swagger.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the issue to add a watcher to. |
| `user_id` | body | `number` | yes | ID of the user to add as a watcher. |
