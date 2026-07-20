# Create Reader with KnowledgeOwl

## Endpoint

- **Method:** `POST`
- **Path:** `/reader.json`
- **Base URL:** `https://app.knowledgeowl.com/api/head`
- **Official documentation:** [Create Reader](https://support.knowledgeowl.com/help/api-endpoint-reference)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `temp-pass` | body | `string` | yes |
| `pw-type` | body | `string` | yes |
| `username` | body | `string` | yes |
| `status` | body | `string` | yes |
| `projects[]` | body | `array<string>` | yes |
