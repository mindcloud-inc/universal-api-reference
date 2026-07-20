# Upsert Tags with Virtually

Creates or updates tags in Virtually.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v2/orgs/:orgId/tags`
- **Base URL:** `https://app.tryvirtually.com`
- **Official documentation:** [Upsert Tags](https://app.tryvirtually.com/api/docs#/Tags/TagsController_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags[]` | body | `array<object>` | yes | Tags to create or update. |
| `tags[].name` | body | `string` | yes | The tag name. |
