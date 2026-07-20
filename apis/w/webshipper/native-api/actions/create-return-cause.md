# Create Return Cause with Webshipper

Creates a return cause in Webshipper.

## Endpoint

- **Method:** `POST`
- **Path:** `/return_causes`
- **Base URL:** `https://{accountName}.api.webshipper.io/v2`
- **Official documentation:** [Create Return Cause](https://docs.webshipper.io/#return_causes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.description` | body | `string` | no | Description of the return cause. |
| `data.attributes.limit_refund_methods` | body | `string` | no | Whether refund methods should be limited. |
| `data.attributes.name` | body | `string` | no | Name of the return cause. |
| `data.attributes.require_comment` | body | `string` | no | Whether a comment is required for this return cause. |
| `data.attributes.support_image_required` | body | `string` | no | Whether a support image is required. |
| `data.relationships.portal.data.id` | body | `string` | no | Return portal ID. |
| `data.type` | body | `string` | yes | Use the default value `return_causes`. |
| `data.relationships.portal.data.type` | body | `string` | yes | Use the default value `return_portals`. |
