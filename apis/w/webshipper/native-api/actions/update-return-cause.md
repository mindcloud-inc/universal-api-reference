# Update Return Cause with Webshipper

Updates a return cause in Webshipper.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/return_causes/:id`
- **Base URL:** `https://{accountName}.api.webshipper.io/v2`
- **Official documentation:** [Update Return Cause](https://docs.webshipper.io/#return_causes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.description` | body | `string` | no | Updated return cause description. |
| `data.attributes.limit_refund_methods` | body | `string` | no | Whether refund methods should be limited. |
| `data.attributes.name` | body | `string` | no | Updated return cause name. |
| `data.attributes.require_comment` | body | `string` | no | Whether a comment is required for this return cause. |
| `data.attributes.support_image_required` | body | `string` | no | Whether a support image is required. |
| `data.id` | body | `string` | no | Repeat the ID value for the JSON:API request body. |
| `id` | path | `string` | no | The return cause ID. |
| `data.type` | body | `string` | yes | Use the default value `return_causes`. |
