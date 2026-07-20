# Create Browsing Task with Yutori

Creates a Yutori browsing task for an automated web workflow.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/browsing/tasks`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Create Browsing Task](https://docs.yutori.com/reference/browsing-create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `task` | body | `string` | yes |
| `start_url` | body | `string` | yes |
| `max_steps` | body | `number` | no |
| `require_auth` | body | `boolean` | no |
| `output_schema` | body | `object` | no |
| `webhook_url` | body | `string` | no |
| `webhook_format` | body | `string` | no |
