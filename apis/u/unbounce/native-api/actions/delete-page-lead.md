# Delete Page Lead with Unbounce

Deletes a specific lead from an Unbounce page.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/pages/:page_id/leads/:lead_id`
- **Base URL:** `https://api.unbounce.com`
- **Official documentation:** [Delete Page Lead](https://developer.unbounce.com/api_reference/#id_pages__page_id__leads__lead_id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `lead_id` | path | `string` | yes | Unbounce lead ID. |
| `page_id` | path | `string` | yes | Unbounce page ID. |
