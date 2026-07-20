# <img src="https://images.mindcloud.co/apps/icons/lex-fridman-podcast_1776430046926.png" alt="Lex Fridman Podcast logo" width="28" height="28"> Lex Fridman Podcast: Universal API

Read Lex Fridman podcast posts, pages, media, and site metadata

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lexFridmanPodcast/latest
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lexfridman.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Category](actions/get-category.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lexFridmanPodcast/latest/actions/get-category?connectionId=$CONNECTION_ID&id=3392" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from Lex Fridman Podcast. |
| [Get Content Type](actions/get-content-type.md) | GET | Retrieves a content type from Lex Fridman Podcast. |
| [Get OEmbed Embed](actions/get-oembed-embed.md) | GET | Retrieves oEmbed data for a URL from Lex Fridman Podcast. |
| [Get OEmbed Namespace Info](actions/get-oembed-namespace-info.md) | GET | Retrieves oEmbed namespace details from Lex Fridman Podcast. |
| [Get Page](actions/get-page.md) | GET | Retrieves a page from Lex Fridman Podcast. |
| [Get Post](actions/get-post.md) | GET | Retrieves a post from Lex Fridman Podcast. |
| [Get Site API Root](actions/get-site-api-root.md) | GET | Retrieves site API root details from Lex Fridman Podcast. |
| [Get Status](actions/get-status.md) | GET | Retrieves a content status from Lex Fridman Podcast. |
| [Get Taxonomy](actions/get-taxonomy.md) | GET | Retrieves a taxonomy from Lex Fridman Podcast. |
| [Get WordPress Namespace Info](actions/get-wordpress-namespace-info.md) | GET | Retrieves WordPress namespace details from Lex Fridman Podcast. |
| [List Blocks](actions/list-blocks.md) | GET | Retrieves blocks from Lex Fridman Podcast. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from Lex Fridman Podcast. |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments from Lex Fridman Podcast. |
| [List Content Types](actions/list-content-types.md) | GET | Retrieves content types from Lex Fridman Podcast. |
| [List Navigation Menus](actions/list-navigation-menus.md) | GET | Retrieves navigation menus from Lex Fridman Podcast. |
| [List Pages](actions/list-pages.md) | GET | Retrieves pages from Lex Fridman Podcast. |
| [List Pattern Categories](actions/list-pattern-categories.md) | GET | Retrieves pattern categories from Lex Fridman Podcast. |
| [List Posts](actions/list-posts.md) | GET | Retrieves posts from Lex Fridman Podcast. |
| [List Posts By Author](actions/list-posts-by-author.md) | GET | Retrieves posts from Lex Fridman Podcast by author. |
| [List Posts By Category](actions/list-posts-by-category.md) | GET | Retrieves posts from Lex Fridman Podcast by category. |
| [List Statuses](actions/list-statuses.md) | GET | Retrieves content statuses from Lex Fridman Podcast. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Lex Fridman Podcast. |
| [List Taxonomies](actions/list-taxonomies.md) | GET | Retrieves taxonomies from Lex Fridman Podcast. |
| [Search Categories](actions/search-categories.md) | GET | Finds categories in Lex Fridman Podcast by search term. |
| [Search Content](actions/search-content.md) | GET | Finds content in Lex Fridman Podcast by search term. |
| [Search Pages](actions/search-pages.md) | GET | Finds pages in Lex Fridman Podcast by search term. |
| [Search Posts](actions/search-posts.md) | GET | Finds posts in Lex Fridman Podcast by search term. |
| [Search Tags](actions/search-tags.md) | GET | Finds tags in Lex Fridman Podcast by search term. |
| [Search Terms](actions/search-terms.md) | GET | Finds terms in Lex Fridman Podcast by search term. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Media](actions/get-media.md) | GET | Retrieves a media item from Lex Fridman Podcast. |
| [List Media](actions/list-media.md) | GET | Retrieves media items from Lex Fridman Podcast. |
| [Search Media](actions/search-media.md) | GET | Finds media items in Lex Fridman Podcast by search term. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Lex Fridman Podcast. |
| [Search Users](actions/search-users.md) | GET | Finds users in Lex Fridman Podcast by search term. |

