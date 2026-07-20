# <img src="https://images.mindcloud.co/apps/icons/longreads_1776428055419.png" alt="Longreads logo" width="28" height="28"> Longreads: Universal API

Read Longreads stories, pages, authors, metadata, and recommendations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/longreads/latest
- **Category:** Website & App Building / CMS
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://longreads.com/
- **Vendor API docs:** https://longreads.com/wp-json/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Category](actions/get-category.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/longreads/latest/actions/get-category?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Category](actions/get-category.md) | GET | Retrieves a Longreads category by ID. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from the Longreads site. |
| [List Categories By Slug](actions/list-categories-by-slug.md) | GET | Finds Longreads categories by category slug. |
| [Search Categories](actions/search-categories.md) | GET | Finds Longreads categories by search text. |

### Coauthor

| Action | Method | Description |
| --- | --- | --- |
| [Get Coauthor](actions/get-coauthor.md) | GET | Retrieves a Longreads coauthor by nicename. |
| [List Coauthors For Post](actions/list-coauthors-for-post.md) | GET | Retrieves Longreads coauthors for a specific post. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments from the Longreads site. |
| [List Comments For Post](actions/list-comments-for-post.md) | GET | Retrieves Longreads comments for a specific post. |
| [Search Comments](actions/search-comments.md) | GET | Finds Longreads comments by search text. |

### Guest Author

| Action | Method | Description |
| --- | --- | --- |
| [Get Guest Author](actions/get-guest-author.md) | GET | Retrieves a Longreads guest author by ID. |
| [List Guest Authors](actions/list-guest-authors.md) | GET | Retrieves guest author profiles from Longreads. |
| [Search Guest Authors](actions/search-guest-authors.md) | GET | Finds Longreads guest authors by search text. |

### Media

| Action | Method | Description |
| --- | --- | --- |
| [Get Media](actions/get-media.md) | GET | Retrieves a Longreads media item by ID. |
| [List Media](actions/list-media.md) | GET | Retrieves media items from the Longreads site. |
| [Search Media](actions/search-media.md) | GET | Finds Longreads media items by search text. |

### Oembed Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get OEmbed Metadata](actions/get-oembed-metadata.md) | GET | Retrieves Longreads oEmbed metadata for a URL. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Page](actions/get-page.md) | GET | Retrieves a Longreads page by ID. |
| [List Pages](actions/list-pages.md) | GET | Retrieves pages from the Longreads site. |
| [List Pages By Slug](actions/list-pages-by-slug.md) | GET | Finds Longreads pages by page slug. |
| [Search Pages](actions/search-pages.md) | GET | Finds Longreads pages by search text. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [Get Post](actions/get-post.md) | GET | Retrieves a Longreads post by ID. |
| [List Posts](actions/list-posts.md) | GET | Retrieves published posts from the Longreads site. |
| [List Posts By Category](actions/list-posts-by-category.md) | GET | Retrieves Longreads posts in a specific category. |
| [List Posts By Slug](actions/list-posts-by-slug.md) | GET | Finds Longreads posts by post slug. |
| [List Posts By Tag](actions/list-posts-by-tag.md) | GET | Retrieves Longreads posts with a specific tag. |
| [List Posts Published After Date](actions/list-posts-published-after-date.md) | GET | Retrieves Longreads posts published after a date. |
| [List Posts Published Before Date](actions/list-posts-published-before-date.md) | GET | Retrieves Longreads posts published before a date. |
| [Search Posts](actions/search-posts.md) | GET | Finds Longreads posts by search text. |

### Post Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Post Type](actions/get-post-type.md) | GET | Retrieves a post type definition from Longreads. |
| [Get Post Type Index](actions/get-post-type-index.md) | GET | Retrieves post type definitions from Longreads. |

### Recommendation

| Action | Method | Description |
| --- | --- | --- |
| [Get Longreads Recommendations](actions/get-longreads-recommendations.md) | GET | Retrieves Longreads article recommendations by topic. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Site Content](actions/search-site-content.md) | GET | Finds Longreads site content by search text. |

### Seo Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Yoast Head Metadata](actions/get-yoast-head-metadata.md) | GET | Retrieves Longreads Yoast head metadata for a URL. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a Longreads tag by ID. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from the Longreads site. |
| [List Tags By Slug](actions/list-tags-by-slug.md) | GET | Finds Longreads tags by tag slug. |
| [Search Tags](actions/search-tags.md) | GET | Finds Longreads tags by search text. |

### Taxonomy

| Action | Method | Description |
| --- | --- | --- |
| [Get Taxonomy](actions/get-taxonomy.md) | GET | Retrieves a taxonomy definition from Longreads. |
| [Get Taxonomy Index](actions/get-taxonomy-index.md) | GET | Retrieves taxonomy definitions from the Longreads site. |

### Web App Manifest

| Action | Method | Description |
| --- | --- | --- |
| [Get Web App Manifest](actions/get-web-app-manifest.md) | GET | Retrieves the Longreads web app manifest. |

