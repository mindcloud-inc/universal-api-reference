# Create Page Lead with Unbounce

Creates a lead for an Unbounce page.

## Endpoint

- **Method:** `POST`
- **Path:** `/pages/:page_id/leads`
- **Base URL:** `https://api.unbounce.com`
- **Official documentation:** [Create Page Lead](https://developer.unbounce.com/api_reference/#id_pages__page_id__leads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_submission` | body | `object` | yes | Lead submission payload. Include variant_id and form_data field arrays. |
| `page_id` | path | `string` | yes | Unbounce page ID. |
