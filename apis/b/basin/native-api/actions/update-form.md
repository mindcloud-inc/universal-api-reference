# Update Form with Basin

Updates an existing form in Basin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/forms/:id`
- **Base URL:** `https://usebasin.com`
- **Official documentation:** [Update Form](https://usebasin.com/api_docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the form to update. |
| `form` | body | `object` | no | Form fields to update. |
| `form.name` | body | `string` | no | New form name. |
| `form.project_id` | body | `number` | no | Project that owns the form. |
| `form.timezone` | body | `string` | no | Form timezone. |
| `form.redirect_url` | body | `string` | no | Redirect URL after submission. |
| `form.notification_emails` | body | `string` | no | Notification recipient emails. |
| `form.autoreply` | body | `boolean` | no | Whether autoreply is enabled. |
| `form.autoreply_body` | body | `string` | no | Autoresponse email body. |
