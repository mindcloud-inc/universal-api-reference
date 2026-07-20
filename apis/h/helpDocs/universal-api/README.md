# <img src="https://images.mindcloud.co/apps/icons/help-docs_1776114242982.png" alt="HelpDocs logo" width="28" height="28"> HelpDocs: Universal API

Create, organize, and analyze your knowledge base content

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/helpDocs/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.helpdocs.io/
- **Vendor API docs:** https://apidocs.helpdocs.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Articles](actions/list-articles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDocs/latest/actions/list-articles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Article

| Action | Method | Description |
| --- | --- | --- |
| [Create Article](actions/create-article.md) | POST | Creates a new article in HelpDocs. |
| [Delete Article](actions/delete-article.md) | DELETE | Deletes an existing article from HelpDocs. |
| [Get Article](actions/get-article.md) | GET | Retrieves an article from HelpDocs. |
| [List Articles](actions/list-articles.md) | GET | Retrieves articles from HelpDocs. |
| [Update Article](actions/update-article.md) | PUT | Updates an existing article in HelpDocs. |

### Article Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Get Article Feedback](actions/get-article-feedback.md) | GET | Retrieves article feedback from HelpDocs. |

### Article Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Articles](actions/search-articles.md) | GET | Finds articles in HelpDocs by search query. |

### Article Version

| Action | Method | Description |
| --- | --- | --- |
| [Get Article Versions](actions/get-article-versions.md) | GET | Retrieves article versions from HelpDocs. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a new category in HelpDocs. |
| [Delete Category](actions/delete-category.md) | DELETE | Deletes an existing category from HelpDocs. |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from HelpDocs. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from HelpDocs. |
| [Update Category](actions/update-category.md) | PUT | Updates an existing category in HelpDocs. |

### Chatbot Source Page

| Action | Method | Description |
| --- | --- | --- |
| [Generate Chatbot Source Page](actions/generate-chatbot-source-page.md) | GET | Generates a chatbot source page from HelpDocs. |

### Clip

| Action | Method | Description |
| --- | --- | --- |
| [Create Clip](actions/create-clip.md) | POST | Creates a new clip in HelpDocs. |
| [Delete Clip](actions/delete-clip.md) | DELETE | Deletes an existing clip from HelpDocs. |
| [Get Clip](actions/get-clip.md) | GET | Retrieves a clip from HelpDocs. |
| [Update Clip](actions/update-clip.md) | PUT | Updates an existing clip in HelpDocs. |

### Permission Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in HelpDocs. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from HelpDocs. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from HelpDocs. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in HelpDocs. |

### Search Term

| Action | Method | Description |
| --- | --- | --- |
| [Get Search Terms](actions/get-search-terms.md) | GET | Retrieves search terms from HelpDocs. |

### Time Series Data

| Action | Method | Description |
| --- | --- | --- |
| [Get Aggregate Time Series Data](actions/get-aggregate-time-series-data.md) | GET | Retrieves aggregate time series data from HelpDocs. |

### Top Article

| Action | Method | Description |
| --- | --- | --- |
| [Get Top Articles](actions/get-top-articles.md) | GET | Retrieves top articles from HelpDocs. |

