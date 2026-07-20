# Delete Reusable Template Tag with RightSignature

Deletes a tag from a RightSignature reusable template.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/reusable_templates/:reusable_template_id/tags`
- **Base URL:** `https://api.rightsignature.com/public/v2`
- **Official documentation:** [Delete Reusable Template Tag](https://api.rightsignature.com/documentation/resources/v2/reusable_template_tags/destroy.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | body | `string` | yes | Tag name is required |
| `reusable_template_id` | path | `string` | yes | Reusable Template Id value |
