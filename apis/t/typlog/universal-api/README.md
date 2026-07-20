# <img src="https://images.mindcloud.co/apps/icons/typlog_1774976080844.png" alt="Typlog logo" width="28" height="28"> Typlog: Universal API

Typlog is a blogging and podcast hosting platform for managing sites, posts, episodes, pages, subscribers, metrics, and webhooks through the Typlog API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/typlog/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://typlog.com
- **Vendor API docs:** https://api.typlog.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sites](actions/list-sites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typlog/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Author

| Action | Method | Description |
| --- | --- | --- |
| [Get Author](actions/get-author.md) | GET | Retrieves a Typlog author by ID. |
| [List Authors](actions/list-authors.md) | GET | Retrieves authors from Typlog. |

### Content

| Action | Method | Description |
| --- | --- | --- |
| [Save Page Content](actions/save-page-content.md) | PUT | Saves content for a Typlog page. |
| [Save Post Content](actions/save-post-content.md) | PUT | Saves content for a Typlog post. |

### Episode

| Action | Method | Description |
| --- | --- | --- |
| [Create Episode](actions/create-episode.md) | POST | Creates a new episode in Typlog. |
| [Get Episode](actions/get-episode.md) | GET | Retrieves a Typlog episode by ID. |
| [List Episodes](actions/list-episodes.md) | GET | Retrieves episodes from Typlog. |
| [Save Episode Content](actions/save-episode-content.md) | PUT | Saves content for a Typlog episode. |
| [Set Episode Status](actions/set-episode-status.md) | PUT | Updates the status of a Typlog episode. |
| [Update Episode](actions/update-episode.md) | PUT |  |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST | Creates a new page in Typlog. |
| [Get Page](actions/get-page.md) | GET | Retrieves a Typlog page by ID. |
| [List Pages](actions/list-pages.md) | GET | Retrieves pages from Typlog. |
| [Update Page](actions/update-page.md) | PUT |  |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Create Post](actions/create-post.md) | POST | Creates a new post in Typlog. |
| [Get Post](actions/get-post.md) | GET | Retrieves a Typlog post by ID. |
| [List Posts](actions/list-posts.md) | GET | Retrieves posts from Typlog. |
| [Update Post](actions/update-post.md) | PUT |  |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Get Site](actions/get-site.md) | GET | Retrieves a Typlog site by ID. |
| [List Sites](actions/list-sites.md) | GET | Retrieves sites from Typlog. |

### Status

| Action | Method | Description |
| --- | --- | --- |
| [Set Page Status](actions/set-page-status.md) | PUT | Updates the status of a Typlog page. |
| [Set Post Status](actions/set-post-status.md) | PUT | Updates the status of a Typlog post. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a Typlog tag by ID. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Typlog. |

