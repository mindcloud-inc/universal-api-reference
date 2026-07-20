# <img src="https://images.mindcloud.co/apps/icons/collected-notes_1775142300000.png" alt="Collected Notes logo" width="28" height="28"> Collected Notes: Universal API

Create, search, and publish markdown notes and sites

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/collectedNotes/latest
- **Category:** Website & App Building / CMS
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://collectednotes.com/
- **Vendor API docs:** https://collectednotes.com/blog/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/collectedNotes/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Note Links HTML](actions/get-note-links-html.md) | GET |  |
| [List Note Links](actions/list-note-links.md) | GET |  |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST |  |
| [Create Note in First Site](actions/create-note-in-first-site.md) | POST |  |
| [Delete Note](actions/delete-note.md) | DELETE |  |
| [Get Note JSON](actions/get-note-json.md) | GET |  |
| [Get Note Markdown](actions/get-note-markdown.md) | GET |  |
| [Get Note Text](actions/get-note-text.md) | GET |  |
| [Get Rendered Note Body](actions/get-rendered-note-body.md) | GET |  |
| [List Note References](actions/list-note-references.md) | GET |  |
| [List Notes](actions/list-notes.md) | GET |  |
| [Reorder Notes](actions/reorder-notes.md) | PUT |  |
| [Search Notes](actions/search-notes.md) | GET |  |
| [Update Note](actions/update-note.md) | PUT |  |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Create Site](actions/create-site.md) | POST |  |
| [Get Site](actions/get-site.md) | GET |  |
| [Get Site JSON](actions/get-site-json.md) | GET |  |
| [Get Site Markdown](actions/get-site-markdown.md) | GET |  |
| [Get Site RSS Feed](actions/get-site-rss-feed.md) | GET |  |
| [List Sites](actions/list-sites.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

