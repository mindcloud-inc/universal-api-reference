# Update Template with DataForms.io

Updates an existing template in DataForms.io.

## Endpoint

- **Method:** `PUT`
- **Path:** `/templates/{template_id}`
- **Base URL:** `https://api.dataforms.io`
- **Official documentation:** [Update Template](https://dataforms.readme.io/reference/show-template-copy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_id` | path | `string` | yes | The DataForms.io template identifier. |
| `name` | body | `string` | no | Template name. Maximum 255 characters. |
| `description` | body | `string` | no | Template description. Maximum 255 characters. |
| `acronym` | body | `string` | no | Template acronym. Maximum 10 characters. |
| `redirect_url` | body | `string` | no | Redirect URL to use after form submission. |
| `layout` | body | `string` | no | Template layout mode. Accepted values: `0`, `1`. |
| `confirm_submit` | body | `boolean` | no | Show a confirmation modal before submission. |
| `show_header` | body | `boolean` | no | Show the header on the form page. |
