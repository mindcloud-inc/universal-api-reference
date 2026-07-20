# Update Document Tags with RightSignature

Replaces tags on an existing RightSignature document.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/:id/update_tags`
- **Base URL:** `https://api.rightsignature.com/public/v2`
- **Official documentation:** [Update Document Tags](https://api.rightsignature.com/documentation/resources/v2/documents/update_tags.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tags` | body | `string` | yes | Key value tags for categorization |
| `id` | path | `string` | yes | Id value |
