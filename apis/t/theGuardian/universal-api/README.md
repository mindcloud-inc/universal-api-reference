# <img src="https://images.mindcloud.co/apps/icons/the-guardian-icon_1776271695308.png" alt="The Guardian logo" width="28" height="28"> The Guardian: Universal API

Access The Guardian Open Platform to search and retrieve published Guardian content, metadata, tags, sections, editions, and individual items.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/theGuardian/latest
- **Category:** Website & App Building / CMS
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://open-platform.theguardian.com/documentation/
- **Vendor API docs:** https://open-platform.theguardian.com/documentation/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Editions](actions/list-editions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/theGuardian/latest/actions/list-editions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Content

| Action | Method | Description |
| --- | --- | --- |
| [Get Content By IDs](actions/get-content-by-ids.md) | GET | Retrieves Guardian content items by ID. |
| [Search Content](actions/search-content.md) | GET | Finds content in The Guardian with optional search filters. |

### Edition

| Action | Method | Description |
| --- | --- | --- |
| [List Editions](actions/list-editions.md) | GET | Finds matching editions in The Guardian. |

### Editors Pick

| Action | Method | Description |
| --- | --- | --- |
| [Get Editors Picks](actions/get-editors-picks.md) | GET | Retrieves editors' picks for a Guardian path. |
| [Get Home Editors Picks](actions/get-home-editors-picks.md) | GET | Retrieves home-page editors' picks from The Guardian. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Item](actions/get-item.md) | GET | Retrieves a Guardian item by path. |
| [Get Next Items](actions/get-next-items.md) | GET | Retrieves the next Guardian search results after an item. |

### Most Viewed Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Home Most Viewed](actions/get-home-most-viewed.md) | GET | Retrieves home-page most-viewed content from The Guardian. |
| [Get Most Viewed](actions/get-most-viewed.md) | GET | Retrieves most-viewed content for a Guardian path. |

### Related Content

| Action | Method | Description |
| --- | --- | --- |
| [Get Related Content](actions/get-related-content.md) | GET | Retrieves related content for a Guardian item. |

### Section

| Action | Method | Description |
| --- | --- | --- |
| [List Sections](actions/list-sections.md) | GET | Finds matching sections in The Guardian. |

### Story Package Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Story Package](actions/get-story-package.md) | GET | Retrieves story package content for a Guardian item. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Finds matching tags in The Guardian. |

