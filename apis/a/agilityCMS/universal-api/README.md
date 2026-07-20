# <img src="https://images.mindcloud.co/apps/icons/19171476_1780947899854.png" alt="Agility CMS logo" width="28" height="28"> Agility CMS: Universal API

Agility CMS is a headless CMS content fetch integration for retrieving pages, content models, lists, items, galleries, redirects, and sync feeds from Agility instances.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/agilityCMS/latest
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://agilitycms.com
- **Vendor API docs:** https://agilitycms.com/docs/developers/content-fetch-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Sitemap Flat (Preview)](actions/get-sitemap-flat-preview.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/agilityCMS/latest/actions/get-sitemap-flat-preview?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [List Categories (Fetch)](actions/list-categories-fetch.md) | GET | Retrieves published categories from Agility CMS. |
| [List Categories (Preview)](actions/list-categories-preview.md) | GET | Retrieves preview categories from Agility CMS. |

### Content Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Content Item (Fetch)](actions/get-content-item-fetch.md) | GET | Retrieves a published content item from Agility CMS. |
| [Get Content Item (Preview)](actions/get-content-item-preview.md) | GET | Retrieves a preview content item from Agility CMS. |
| [Get Content Item V1 (Fetch)](actions/get-content-item-v1-fetch.md) | GET | Retrieves a published content item from Agility CMS v1. |
| [Get Content Item V1 (Preview)](actions/get-content-item-v1-preview.md) | GET | Retrieves a preview content item from Agility CMS v1. |
| [List Content Items (Fetch)](actions/list-content-items-fetch.md) | GET | Retrieves published content items from Agility CMS. |
| [List Content Items (Preview)](actions/list-content-items-preview.md) | GET | Retrieves preview content items from Agility CMS. |
| [List Content Items V1 (Fetch)](actions/list-content-items-v1-fetch.md) | GET | Retrieves published content items from Agility CMS v1. |
| [List Content Items V1 (Preview)](actions/list-content-items-v1-preview.md) | GET | Retrieves preview content items from Agility CMS v1. |

### Content Model

| Action | Method | Description |
| --- | --- | --- |
| [Get Content Models (Fetch)](actions/get-content-models-fetch.md) | GET | Retrieves published content models from Agility CMS. |
| [Get Content Models (Preview)](actions/get-content-models-preview.md) | GET | Retrieves preview content models from Agility CMS. |

### Gallery

| Action | Method | Description |
| --- | --- | --- |
| [Get Gallery (Fetch)](actions/get-gallery-fetch.md) | GET | Retrieves a published gallery from Agility CMS. |
| [Get Gallery (Preview)](actions/get-gallery-preview.md) | GET | Retrieves a preview gallery from Agility CMS. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Page By ID (Fetch)](actions/get-page-by-id-fetch.md) | GET | Retrieves a published page by ID from Agility CMS. |
| [Get Page By ID (Preview)](actions/get-page-by-id-preview.md) | GET | Retrieves a preview page by ID from Agility CMS. |
| [Get Page By ID V1 (Fetch)](actions/get-page-by-id-v1-fetch.md) | GET | Retrieves a published page by ID from Agility CMS v1. |
| [Get Page By ID V1 (Preview)](actions/get-page-by-id-v1-preview.md) | GET | Retrieves a preview page by ID from Agility CMS v1. |
| [Get Page By Path (Fetch)](actions/get-page-by-path-fetch.md) | GET | Retrieves a published page by path from Agility CMS. |
| [Get Page By Path (Preview)](actions/get-page-by-path-preview.md) | GET | Retrieves a preview page by path from Agility CMS. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [List Posts (Fetch)](actions/list-posts-fetch.md) | GET | Retrieves published posts from Agility CMS. |
| [List Posts (Preview)](actions/list-posts-preview.md) | GET | Retrieves preview posts from Agility CMS. |

### Sitemap Node

| Action | Method | Description |
| --- | --- | --- |
| [Get Sitemap Flat (Fetch)](actions/get-sitemap-flat-fetch.md) | GET | Retrieves the published sitemap as a flat list from Agility CMS. |
| [Get Sitemap Flat (Preview)](actions/get-sitemap-flat-preview.md) | GET | Retrieves the preview sitemap as a flat list from Agility CMS. |
| [Get Sitemap Nested (Fetch)](actions/get-sitemap-nested-fetch.md) | GET | Retrieves the published sitemap in nested format from Agility CMS. |
| [Get Sitemap Nested (Preview)](actions/get-sitemap-nested-preview.md) | GET | Retrieves the preview sitemap in nested format from Agility CMS. |

### Sync State

| Action | Method | Description |
| --- | --- | --- |
| [Sync Content Items (Fetch)](actions/sync-content-items-fetch.md) | GET | Retrieves published content item sync data from Agility CMS. |
| [Sync Content Items (Preview)](actions/sync-content-items-preview.md) | GET | Retrieves preview content item sync data from Agility CMS. |
| [Sync Pages (Fetch)](actions/sync-pages-fetch.md) | GET | Retrieves published page sync data from Agility CMS. |
| [Sync Pages (Preview)](actions/sync-pages-preview.md) | GET | Retrieves preview page sync data from Agility CMS. |

### Url Redirection

| Action | Method | Description |
| --- | --- | --- |
| [Get URL Redirections (Fetch)](actions/get-url-redirections-fetch.md) | GET | Retrieves published URL redirections from Agility CMS. |
| [Get URL Redirections (Preview)](actions/get-url-redirections-preview.md) | GET | Retrieves preview URL redirections from Agility CMS. |

