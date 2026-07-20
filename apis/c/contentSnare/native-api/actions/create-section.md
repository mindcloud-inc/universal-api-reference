# Create Section with Content Snare

Creates a section in Content Snare.

## Endpoint

- **Method:** `POST`
- **Path:** `/partner_api/v1/sections`
- **Base URL:** `https://api.contentsnare.com`
- **Official documentation:** [Create Section](https://api.contentsnare.com/partner_api/v1/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Section name. If it isn't set then the source template name is used. |
| `page_id` | body | `string` | yes | Id of a page where a new section should be added |
| `source_template_id` | body | `string` | no | Source section template id (`source_template_id` or `source_template_name` should be set) |
| `source_template_name` | body | `string` | no | Source section template name (`source_template_id` or `source_template_name` should be set) |
