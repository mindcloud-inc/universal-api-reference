# Add Document with Libraria

Add a new document to your library via scraping or raw text.

## Endpoint

- **Method:** `POST`
- **Path:** `/library/:library_id/document`
- **Base URL:** `https://api.libraria.ai`
- **Official documentation:** [Add Document](https://docs.libraria.ai/api-reference/library/create-document)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `library_id` | path | `string` | yes | The ID of the library to add the document to. |
| `url` | body | `string` | no | A URL to scrape into the library. |
| `text` | body | `string` | no | A raw text document to add to the library. |
| `title` | body | `string` | no | The title to use for a raw text document. |
| `sourceUrl` | body | `string` | no | The source URL used for the Learn More snippet. |
| `imageSnippet` | body | `string` | no | The image URL to attach as the document snippet. |
