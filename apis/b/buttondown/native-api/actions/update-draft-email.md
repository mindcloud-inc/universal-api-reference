# Update Draft Email with Buttondown

Updates an existing draft email in Buttondown.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/emails/:id`
- **Base URL:** `https://api.buttondown.com/v1`
- **Official documentation:** [Update Draft Email](https://docs.buttondown.com/api-emails-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Email ID. |
| `subject` | body | `string` | no | Updated draft email subject line. |
| `body` | body | `string` | no | Updated draft email body content. |
| `description` | body | `string` | no | Updated internal description for the draft email. |
| `slug` | body | `string` | no | Updated draft slug. |
| `canonical_url` | body | `string` | no | Updated canonical URL for the email. |
