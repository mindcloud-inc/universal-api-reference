# Update Template with Resend

Updates an existing template in Resend.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/templates/:id`
- **Base URL:** `https://api.resend.com`
- **Official documentation:** [Update Template](https://resend.com/docs/api-reference/templates/update-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Template identifier or alias. |
| `name` | body | `string` | no | Updated template name. |
| `html` | body | `string` | no | Updated HTML content for the template. |
