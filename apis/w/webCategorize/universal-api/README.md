# <img src="https://images.mindcloud.co/apps/icons/images-23_1776776026865.png" alt="WebCategorize logo" width="28" height="28"> WebCategorize: Universal API

WebCategorize classifies URLs and supplied web content in real time using documented REST endpoints for URL categorization, content categorization, tags, feedback, and API key management.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/webCategorize/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://webcategorize.com/
- **Vendor API docs:** https://webcategorize.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List URL Tags](actions/list-url-tags.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/list-url-tags?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Api Key

| Action | Method | Description |
| --- | --- | --- |
| [Create API Key](actions/create-api-key.md) | POST |  |
| [List API Keys](actions/list-api-keys.md) | GET |  |

### Content Categorization

| Action | Method | Description |
| --- | --- | --- |
| [Categorize Content](actions/categorize-content.md) | POST |  |
| [List Content Categorizations](actions/list-content-categorizations.md) | GET |  |
| [Retrieve Content Categorization](actions/retrieve-content-categorization.md) | GET |  |

### Content Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Add Content Feedback](actions/add-content-feedback.md) | POST |  |

### Content Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Content Tags](actions/list-content-tags.md) | GET |  |

### Url Categorization

| Action | Method | Description |
| --- | --- | --- |
| [Categorize URL](actions/categorize-url.md) | POST |  |
| [List URL Categorizations](actions/list-url-categorizations.md) | GET |  |
| [Retrieve URL Categorization](actions/retrieve-url-categorization.md) | GET |  |

### Url Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Add URL Feedback](actions/add-url-feedback.md) | POST |  |

### Url Tag

| Action | Method | Description |
| --- | --- | --- |
| [List URL Tags](actions/list-url-tags.md) | GET |  |

