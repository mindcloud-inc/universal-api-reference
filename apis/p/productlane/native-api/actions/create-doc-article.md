# Create Doc Article with Productlane

Creates a help center article in Productlane.

## Endpoint

- **Method:** `POST`
- **Path:** `/docs/articles`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Create Doc Article](https://productlane.mintlify.dev/docs/api/docs/create-doc-article)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Doc article title. |
| `content` | body | `string` | yes | Markdown content for the doc article. |
| `groupId` | body | `string` | yes | Target docs group ID. |
| `summary` | body | `string` | no | Article summary. |
| `published` | body | `boolean` | no | Whether the article should be published immediately. |
| `language` | body | `string` | no | Language code for the article. |
