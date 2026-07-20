# <img src="https://images.mindcloud.co/apps/icons/t-hehill_1776449355225.png" alt="THE HILL logo" width="28" height="28"> THE HILL: Universal API

Read The Hill news, posts, pages, and media

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tHEHILL/latest
- **Category:** Website & App Building / CMS
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://thehill.com/
- **Vendor API docs:** https://developer.wordpress.org/rest-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Category](actions/get-category.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tHEHILL/latest/actions/get-category?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [List Alerts](actions/list-alerts.md) | GET | Retrieves alert posts from The Hill. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves content categories from The Hill. |

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET | Retrieves a specific category from The Hill. |

### City Tags

| Action | Method | Description |
| --- | --- | --- |
| [List City Tags](actions/list-city-tags.md) | GET | Retrieves city tags from The Hill. |

### Company Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Company Tags](actions/list-company-tags.md) | GET | Retrieves company tags from The Hill. |

### Country Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Country Tags](actions/list-country-tags.md) | GET | Retrieves country tags from The Hill. |

### Email Newsletters

| Action | Method | Description |
| --- | --- | --- |
| [List Email Newsletters](actions/list-email-newsletters.md) | GET | Retrieves email newsletters from The Hill. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves event posts from The Hill. |

### Events Facts Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Events Facts Tags](actions/list-events-facts-tags.md) | GET | Retrieves events facts tags from The Hill. |

### Feed Posts

| Action | Method | Description |
| --- | --- | --- |
| [List Feed Posts](actions/list-feed-posts.md) | GET | Retrieves feed posts from The Hill. |

### Future America Posts

| Action | Method | Description |
| --- | --- | --- |
| [List Future America Posts](actions/list-future-america-posts.md) | GET | Retrieves Future America posts from The Hill. |

### Galleries

| Action | Method | Description |
| --- | --- | --- |
| [List Galleries](actions/list-galleries.md) | GET | Retrieves gallery posts from The Hill. |

### Hilltv Posts

| Action | Method | Description |
| --- | --- | --- |
| [List HillTV Posts](actions/list-hilltv-posts.md) | GET | Retrieves HillTV posts from The Hill. |

### Link Posts

| Action | Method | Description |
| --- | --- | --- |
| [List Link Posts](actions/list-link-posts.md) | GET | Retrieves link posts from The Hill. |

### Media

| Action | Method | Description |
| --- | --- | --- |
| [Get Media](actions/get-media.md) | GET | Retrieves a specific media item from The Hill. |
| [List Media](actions/list-media.md) | GET | Retrieves media items from The Hill. |

### Navigation

| Action | Method | Description |
| --- | --- | --- |
| [List Navigation](actions/list-navigation.md) | GET | Retrieves navigation items from The Hill. |

### Newsletter Posts

| Action | Method | Description |
| --- | --- | --- |
| [List Newsletter Posts](actions/list-newsletter-posts.md) | GET | Retrieves newsletter posts from The Hill. |

### Nota

| Action | Method | Description |
| --- | --- | --- |
| [List Nota](actions/list-nota.md) | GET | Retrieves Nota posts from The Hill. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Page](actions/get-page.md) | GET | Retrieves a specific page from The Hill. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [List Pages](actions/list-pages.md) | GET | Retrieves published pages from The Hill. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Get Post](actions/get-post.md) | GET | Retrieves a specific post from The Hill. |

### Posts

| Action | Method | Description |
| --- | --- | --- |
| [List Posts](actions/list-posts.md) | GET | Retrieves published posts from The Hill. |

### Rss Feed

| Action | Method | Description |
| --- | --- | --- |
| [RSS Feed](actions/rss-feed.md) | GET | Retrieves The Hill's news RSS feed. |

### Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Search Content](actions/search-content.md) | GET | Finds content in The Hill by search query. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Statuses](actions/list-statuses.md) | GET | Retrieves content statuses from The Hill. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a specific tag from The Hill. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Retrieves content tags from The Hill. |

### Vertical Posts

| Action | Method | Description |
| --- | --- | --- |
| [List Vertical Posts](actions/list-vertical-posts.md) | GET | Retrieves vertical posts from The Hill. |

### Videos

| Action | Method | Description |
| --- | --- | --- |
| [List Videos](actions/list-videos.md) | GET | Retrieves video posts from The Hill. |

