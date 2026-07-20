# Add Or Update Reusable Template Tags with RightSignature

Adds or updates tags on a RightSignature reusable template.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/reusable_templates/:reusable_template_id/tags`
- **Base URL:** `https://api.rightsignature.com/public/v2`
- **Official documentation:** [Add Or Update Reusable Template Tags](https://api.rightsignature.com/documentation/resources/v2/reusable_template_tags/update.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags` | body | `list<object>` | yes | Optional key value tags for categorization |
| `tags[tag_name]` | body | `string` | yes | Tag name is required |
| `tags[value]` | body | `string` | no | Optional value for the tag |
| `reusable_template_id` | path | `string` | yes | Reusable Template Id value |
