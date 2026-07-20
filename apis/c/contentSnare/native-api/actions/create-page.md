# Create Page with Content Snare

Creates a page in Content Snare.

## Endpoint

- **Method:** `POST`
- **Path:** `/partner_api/v1/pages`
- **Base URL:** `https://api.contentsnare.com`
- **Official documentation:** [Create Page](https://api.contentsnare.com/partner_api/v1/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Page name. If it isn't set then the source template name is used. |
| `request_id` | body | `string` | yes | Id of a request where a new page should be added |
| `source_template_id` | body | `string` | no | Source page template id (`source_template_id` or `source_template_name` should be set) |
| `source_template_name` | body | `string` | no | Source page template name (`source_template_id` or `source_template_name` should be set) |
