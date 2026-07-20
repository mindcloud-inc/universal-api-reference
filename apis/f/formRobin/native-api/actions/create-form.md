# Create Form with FormRobin

Creates a new form in FormRobin.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms`
- **Base URL:** `https://formrobin.com/api/v1`
- **Official documentation:** [Create Form](https://formrobin.com/developer/docs/#tag/Forms/paths/~1forms/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `folder_id` | body | `number` | no |
| `data` | body | `object` | no |
| `email_notifications_enabled` | body | `boolean` | no |
| `redirect_url` | body | `string` | no |
| `webhook_url` | body | `string` | no |
