# Create Project Webhook with Priority Matrix

Creates a webhook for a Priority Matrix project.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/hook/`
- **Base URL:** `https://sync.appfluence.com`
- **Official documentation:** [Create Project Webhook](https://sync.appfluence.com/developer/guide/#webhooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `event` | body | `string` | yes | Webhook event, for example item.created. |
| `target` | body | `string` | yes | Webhook delivery URL. |
| `project` | body | `string` | yes | Project resource URI, for example /api/v1/project/234/. |
