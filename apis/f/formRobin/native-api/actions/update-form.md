# Update Form with FormRobin

Updates an existing form in FormRobin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/forms/{{id}}`
- **Base URL:** `https://formrobin.com/api/v1`
- **Official documentation:** [Update Form](https://formrobin.com/developer/docs/#tag/Forms/paths/~1forms~1{id}/put)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The FormRobin form ID to update. |
| `name` | body | `string` | no | The form name. |
| `folder_id` | body | `number` | no | The destination folder ID for the form. |
| `data` | body | `object` | no | Form configuration data. |
| `email_notifications_enabled` | body | `boolean` | no | Whether email notifications are enabled for the form. |
| `redirect_url` | body | `string` | no | The URL to redirect to after form submission. |
| `webhook_url` | body | `string` | no | The webhook URL that receives form submissions. |
