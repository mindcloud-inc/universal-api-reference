# <img src="https://images.mindcloud.co/apps/icons/document360_1774379094380.png" alt="Document360 logo" width="28" height="28"> Document360: Universal API

Manage knowledge base articles, categories, readers, and teams

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/document360/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://document360.com
- **Vendor API docs:** https://apidocs.document360.com/apidocs/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Project Versions](actions/list-project-versions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/document360/latest/actions/list-project-versions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Article

| Action | Method | Description |
| --- | --- | --- |
| [Create Article](actions/create-article.md) | POST |  |
| [Fork Article](actions/fork-article.md) | PUT |  |
| [Get Article](actions/get-article.md) | GET |  |
| [Get Article by URL](actions/get-article-by-url.md) | GET |  |
| [Get Article by Version](actions/get-article-by-version.md) | GET |  |
| [List Articles in Project Version](actions/list-articles-in-project-version.md) | GET |  |
| [Publish Article](actions/publish-article.md) | PUT |  |
| [Update Article](actions/update-article.md) | PUT |  |

### Article Version

| Action | Method | Description |
| --- | --- | --- |
| [List Article Versions](actions/list-article-versions.md) | GET |  |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST |  |
| [Fork Category Page](actions/fork-category-page.md) | PUT |  |
| [Get Category](actions/get-category.md) | GET |  |
| [List Categories in Project Version](actions/list-categories-in-project-version.md) | GET |  |
| [Publish Category](actions/publish-category.md) | PUT |  |
| [Update Category](actions/update-category.md) | PUT |  |
| [Update Category Type](actions/update-category-type.md) | PUT |  |

### Category Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Category Page](actions/get-category-page.md) | GET |  |

### Content

| Action | Method | Description |
| --- | --- | --- |
| [Update Category Page Content](actions/update-category-page-content.md) | PUT |  |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Get Document by URL Path](actions/get-document-by-url-path.md) | GET |  |

### Language

| Action | Method | Description |
| --- | --- | --- |
| [List Version Languages](actions/list-version-languages.md) | GET |  |

### Project Version

| Action | Method | Description |
| --- | --- | --- |
| [List Project Versions](actions/list-project-versions.md) | GET |  |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Articles in Project Version](actions/search-articles-in-project-version.md) | GET |  |

### Translation Status

| Action | Method | Description |
| --- | --- | --- |
| [Search Articles by Translation Status](actions/search-articles-by-translation-status.md) | GET |  |

### Workflow Status

| Action | Method | Description |
| --- | --- | --- |
| [List Workflow Statuses](actions/list-workflow-statuses.md) | GET |  |

