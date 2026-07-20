# <img src="https://images.mindcloud.co/apps/icons/product-fruits_1774017275522.png" alt="Product Fruits logo" width="28" height="28"> Product Fruits: Universal API

Track events, manage knowledge bases, and capture user feedback

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/productFruits/latest
- **Category:** Support / Customer Success
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://productfruits.com
- **Vendor API docs:** https://help.productfruits.com/en/article/rest-api-authentication

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Knowledge Base Categories](actions/list-knowledge-base-categories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/list-knowledge-base-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Track Event](actions/track-event.md) | POST |  |

### Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Create Feedback](actions/create-feedback.md) | POST |  |

### Knowledge Base Article

| Action | Method | Description |
| --- | --- | --- |
| [Delete Article Content by Language](actions/delete-article-content-by-language.md) | DELETE |  |
| [Delete Knowledge Base Article](actions/delete-knowledge-base-article.md) | DELETE |  |
| [Import Knowledge Base Articles](actions/import-knowledge-base-articles.md) | PUT |  |
| [List Knowledge Base Articles](actions/list-knowledge-base-articles.md) | GET |  |

### Knowledge Base Article Content

| Action | Method | Description |
| --- | --- | --- |
| [Delete Article Content Version](actions/delete-article-content-version.md) | DELETE |  |

### Knowledge Base Category

| Action | Method | Description |
| --- | --- | --- |
| [Delete Knowledge Base Category](actions/delete-knowledge-base-category.md) | DELETE |  |
| [Get Knowledge Base Category](actions/get-knowledge-base-category.md) | GET |  |
| [Import Knowledge Base Categories](actions/import-knowledge-base-categories.md) | PUT |  |
| [List Knowledge Base Categories](actions/list-knowledge-base-categories.md) | GET |  |
| [Update Knowledge Base Category](actions/update-knowledge-base-category.md) | PUT |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Delete User](actions/delete-user.md) | DELETE |  |
| [Identify User](actions/identify-user.md) | PUT |  |

