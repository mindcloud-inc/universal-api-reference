# <img src="https://images.mindcloud.co/apps/icons/knowledge-owl_1774982247205.png" alt="KnowledgeOwl logo" width="28" height="28"> KnowledgeOwl: Universal API

KnowledgeOwl through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/knowledgeOwl/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.knowledgeowl.com
- **Vendor API docs:** https://support.knowledgeowl.com/help/use-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Categories](actions/list-categories.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/knowledgeOwl/latest/actions/list-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST |  |
| [Delete Category](actions/delete-category.md) | DELETE |  |
| [Get Category](actions/get-category.md) | GET |  |
| [List Categories](actions/list-categories.md) | GET |  |
| [Update Category](actions/update-category.md) | PUT |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create File](actions/create-file.md) | POST |  |
| [Delete File](actions/delete-file.md) | DELETE |  |
| [Get File](actions/get-file.md) | GET |  |
| [List Files](actions/list-files.md) | GET |  |
| [Replace File Contents](actions/replace-file-contents.md) | PUT |  |
| [Update File](actions/update-file.md) | PUT |  |

### Knowledge Articles

| Action | Method | Description |
| --- | --- | --- |
| [Create Article](actions/create-article.md) | POST |  |
| [Delete Article](actions/delete-article.md) | DELETE |  |
| [Get Article](actions/get-article.md) | GET |  |
| [List Articles](actions/list-articles.md) | GET |  |
| [Update Article](actions/update-article.md) | PUT |  |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST |  |
| [Delete Tag](actions/delete-tag.md) | DELETE |  |
| [Get Tag](actions/get-tag.md) | GET |  |
| [List Tags](actions/list-tags.md) | GET |  |
| [Update Tag](actions/update-tag.md) | PUT |  |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Create Reader](actions/create-reader.md) | POST |  |
| [Delete Reader](actions/delete-reader.md) | DELETE |  |
| [Get Reader](actions/get-reader.md) | GET |  |
| [List Readers](actions/list-readers.md) | GET |  |
| [Update Reader](actions/update-reader.md) | PUT |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook Subscription](actions/create-webhook-subscription.md) | POST |  |
| [Delete Webhook Subscription](actions/delete-webhook-subscription.md) | DELETE |  |
| [Get Webhook Subscription](actions/get-webhook-subscription.md) | GET |  |
| [List Webhook Subscriptions](actions/list-webhook-subscriptions.md) | GET |  |
| [Update Webhook Subscription](actions/update-webhook-subscription.md) | PUT |  |

