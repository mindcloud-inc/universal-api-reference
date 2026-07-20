# Create Form with Basin

Creates a new form in Basin.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/forms/`
- **Base URL:** `https://usebasin.com`
- **Official documentation:** [Create Form](https://usebasin.com/api_docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form` | body | `object` | no | Form fields to create. |
| `form.name` | body | `string` | yes | Form name. |
| `form.project_id` | body | `number` | no | Project ID for the new form. |
| `form.timezone` | body | `string` | no | Form timezone. |
| `form.redirect_url` | body | `string` | no | Redirect URL after submission. |
| `form.notification_emails` | body | `string` | no | Notification recipient emails. |
| `form.autoreply` | body | `boolean` | no | Whether autoreply is enabled. |
| `form.autoreply_body` | body | `string` | no | Autoresponse email body. |
