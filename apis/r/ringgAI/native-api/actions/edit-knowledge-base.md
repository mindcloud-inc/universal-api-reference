# Edit Knowledge Base with Ringg AI

Updates an existing knowledge base in Ringg AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/external/kb`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`
- **Official documentation:** [Edit Knowledge Base](https://docs.ringg.ai/api-reference/endpoint/kb/edit-knowledge-base)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `kb_id` | body | `string` | yes | (Required) ID of the knowledge base to edit |
| `files_to_remove` | body | `string` | no | (Optional) JSON string array of file IDs to remove |
| `urls_to_remove` | body | `string` | no | (Optional) JSON string array of URLs to remove |
| `faqs_to_remove` | body | `string` | no | (Optional) JSON string array of FAQ IDs to remove |
| `new_files[]` | body | `array<string>` | no | (Optional) Array of new files to upload |
| `new_urls` | body | `string` | no | (Optional) JSON string array of new URLs to add |
| `new_faqs` | body | `string` | no | (Optional) JSON string array of new FAQ objects |
| `new_files_metadata` | body | `string` | no | (Optional) JSON string object with metadata for new files |
