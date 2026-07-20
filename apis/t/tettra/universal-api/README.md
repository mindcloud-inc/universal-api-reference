# <img src="https://images.mindcloud.co/apps/icons/tettra-icon_1774906823552.png" alt="Tettra logo" width="28" height="28"> Tettra: Universal API

Search, create, and manage Tettra knowledge pages and categories

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tettra/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tettra.com
- **Vendor API docs:** https://support.tettra.com/api-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Pages](actions/search-pages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tettra/latest/actions/search-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Create Category](actions/create-category.md) | POST | Creates a new category in Tettra. |

### Category Item

| Action | Method | Description |
| --- | --- | --- |
| [List Category Items](actions/list-category-items.md) | GET | Retrieves category items from Tettra. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST | Creates a new page in Tettra. |
| [Search Pages](actions/search-pages.md) | GET | Finds pages in Tettra by search term. |
| [Update Page](actions/update-page.md) | PUT | Updates an existing page in Tettra. |

### Question

| Action | Method | Description |
| --- | --- | --- |
| [Create Question](actions/create-question.md) | POST | Creates a new question in Tettra. |

### Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Suggest New Page](actions/suggest-new-page.md) | POST | Creates a new page suggestion in Tettra. |
| [Suggest Page Update](actions/suggest-page-update.md) | POST | Creates a page update suggestion in Tettra. |

