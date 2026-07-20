# Create or Update URL Mapping with Dynamic Content Snippet

Updates a URL mapping in Dynamic Content Snippet, or creates one if needed.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/mappings`
- **Base URL:** `https://app.contentsnip.com`
- **Official documentation:** [Create or Update URL Mapping](https://contentsnip.com/documentation.htm)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | URL of the webpage where content will appear. |
| `htmlContent` | body | `string` | yes | HTML content to display at the target URL. ContentSnip allows an empty string to delete content. |
