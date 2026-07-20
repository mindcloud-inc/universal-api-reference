# Create Template with BigMailer

Creates a new template in a BigMailer brand.

## Endpoint

- **Method:** `POST`
- **Path:** `/brands/:brand_id/templates`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [Create Template](https://docs.bigmailer.io/reference/createtemplate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand to create the template in. |
| `name` | body | `string` | yes | Name of the template. |
| `type` | body | `string` | yes | Type of template to create. |
| `shared_with_account` | body | `boolean` | no | Whether the template should be shared across the account. |
| `html` | body | `string` | yes | HTML content of the template. |
