# Create Knowledge Base with Ringg AI

Creates a knowledge base in Ringg AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/external/kb`
- **Base URL:** `https://prod-api.ringg.ai/ca/api/v0`
- **Official documentation:** [Create Knowledge Base](https://docs.ringg.ai/api-reference/endpoint/kb/create-knowledge-base)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `kb_name` | body | `string` | yes | (Required) Name of the knowledge base |
| `files[]` | body | `array<string>` | no | (Optional) Array of files to upload (max 10 files, 2 MB each, 5 MB total) |
| `urls` | body | `string` | no | (Optional) JSON string array of URLs to index (max 20 URLs) |
| `faqs` | body | `string` | no | (Optional) JSON string array of FAQ objects |
