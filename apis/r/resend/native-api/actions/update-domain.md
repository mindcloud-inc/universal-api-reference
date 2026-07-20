# Update Domain with Resend

Updates an existing domain in Resend.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/domains/:id`
- **Base URL:** `https://api.resend.com`
- **Official documentation:** [Update Domain](https://resend.com/docs/api-reference/domains/update-domain)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string<string>` | yes |
| `open_tracking` | body | `boolean` | no |
| `click_tracking` | body | `boolean` | no |
| `tls` | body | `string` | no |
| `region` | body | `string` | no |
