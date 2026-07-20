# Update Email Template with Bento Now

Updates an email template subject or HTML in Bento Now.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/fetch/emails/templates/:id`
- **Base URL:** `https://app.bentonow.com/api`
- **Official documentation:** [Update Email Template](https://bentonow.com/docs/email_templates_api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email_template.html` | body | `string` | no |
| `email_template.subject` | body | `string` | no |
| `id` | path | `number` | yes |
