# Create Research Task with Yutori

Creates a one-time research task in Yutori.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/research/tasks`
- **Base URL:** `https://api.yutori.com`
- **Official documentation:** [Create Research Task](https://docs.yutori.com/reference/research-create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `query` | body | `string` | yes |
| `mode` | body | `string` | no |
| `user_timezone` | body | `string` | no |
| `user_location` | body | `string` | no |
| `output_schema` | body | `object` | no |
| `skip_email` | body | `boolean` | no |
| `webhook_url` | body | `string` | no |
| `webhook_format` | body | `string` | no |
