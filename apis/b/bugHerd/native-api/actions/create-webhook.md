# Create Webhook with BugHerd

Creates a new webhook in BugHerd.

## Endpoint

- **Method:** `POST`
- **Path:** `webhooks.json`
- **Base URL:** `https://www.bugherd.com/api_v2`
- **Official documentation:** [Create Webhook](https://docs.bugherd.com/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | body | `number` | no |
| `target_url` | body | `string` | yes |
| `event` | body | `string` | yes |
