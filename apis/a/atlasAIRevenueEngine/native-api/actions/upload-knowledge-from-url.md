# Upload Knowledge from URL with Atlas AI Revenue Engine

## Endpoint

- **Method:** `POST`
- **Path:** `/knowledgebase/knowledge-extract`
- **Base URL:** `https://api.youratlas.com/v1/api`
- **Official documentation:** [Upload Knowledge from URL](https://apidocs.youratlas.com/upload-knowledge-from-url-26917882e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | no | Optional campaign ID. |
| `url` | body | `string` | yes | URL to extract knowledge from (URI). |
