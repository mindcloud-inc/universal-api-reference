# <img src="https://images.mindcloud.co/apps/icons/crime-junkie-icon_1776433524358.png" alt="Crime Junkie Podcast logo" width="28" height="28"> Crime Junkie Podcast: Universal API

Access the public Crime Junkie Podcast RSS feed and WordPress JSON API to read episodes, posts, pages, media, taxonomies, authors, and site metadata from the official site.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/crimeJunkiePodcast/latest
- **Actions:** 58
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://crimejunkiepodcast.com/
- **Vendor API docs:** https://crimejunkiepodcast.com/wp-json/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Recent Episodes](actions/list-recent-episodes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crimeJunkiePodcast/latest/actions/list-recent-episodes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (58)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Attachment Category](actions/get-attachment-category.md) | GET | Retrieves an attachment category from Crime Junkie Podcast. |
| [Get Block](actions/get-block.md) | GET | Retrieves a block from Crime Junkie Podcast. |
| [Get Category](actions/get-category.md) | GET | Retrieves a category from Crime Junkie Podcast. |
| [Get Comment](actions/get-comment.md) | GET | Retrieves a comment from Crime Junkie Podcast. |
| [Get Content Type](actions/get-content-type.md) | GET | Retrieves a content type from Crime Junkie Podcast. |
| [Get Dipi Content Category](actions/get-dipi-content-category.md) | GET | Retrieves a Dipi content category from Crime Junkie Podcast. |
| [Get Dipi Media Category](actions/get-dipi-media-category.md) | GET | Retrieves a Dipi media category from Crime Junkie Podcast. |
| [Get Fan Club Episode](actions/get-fan-club-episode.md) | GET | Retrieves a fan club episode from Crime Junkie Podcast. |
| [Get Fan Club Tier](actions/get-fan-club-tier.md) | GET | Retrieves a fan club tier from Crime Junkie Podcast. |
| [Get Good Tag](actions/get-good-tag.md) | GET | Retrieves a good tag from Crime Junkie Podcast. |
| [Get Navigation Menu](actions/get-navigation-menu.md) | GET | Retrieves a navigation menu from Crime Junkie Podcast. |
| [Get OEmbed Embed](actions/get-oembed-embed.md) | GET | Retrieves oEmbed embed data from Crime Junkie Podcast. |
| [Get OEmbed Namespace Info](actions/get-oembed-namespace-info.md) | GET | Retrieves oEmbed namespace information from Crime Junkie Podcast. |
| [Get Page](actions/get-page.md) | GET | Retrieves a page from Crime Junkie Podcast. |
| [Get Pattern Category](actions/get-pattern-category.md) | GET | Retrieves a pattern category from Crime Junkie Podcast. |
| [Get Popup Maker](actions/get-popup-maker.md) | GET | Retrieves a popup maker from Crime Junkie Podcast. |
| [Get Post](actions/get-post.md) | GET | Retrieves a post from Crime Junkie Podcast. |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from Crime Junkie Podcast. |
| [Get Project Category](actions/get-project-category.md) | GET | Retrieves a project category from Crime Junkie Podcast. |
| [Get Project Tag](actions/get-project-tag.md) | GET | Retrieves a project tag from Crime Junkie Podcast. |
| [Get Pruppet](actions/get-pruppet.md) | GET | Retrieves a pruppet from Crime Junkie Podcast. |
| [Get Pruppet Category](actions/get-pruppet-category.md) | GET | Retrieves a pruppet category from Crime Junkie Podcast. |
| [Get Site API Root](actions/get-site-api-root.md) | GET | Retrieves the site API root from Crime Junkie Podcast. |
| [Get Status](actions/get-status.md) | GET | Retrieves a status from Crime Junkie Podcast. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from Crime Junkie Podcast. |
| [Get Taxonomy](actions/get-taxonomy.md) | GET | Retrieves a taxonomy from Crime Junkie Podcast. |
| [Get The Good](actions/get-the-good.md) | GET | Retrieves an entry from The Goods in Crime Junkie Podcast. |
| [Get WordPress Namespace Info](actions/get-wordpress-namespace-info.md) | GET | Retrieves WordPress namespace information from Crime Junkie Podcast. |
| [List Attachment Categories](actions/list-attachment-categories.md) | GET | Retrieves attachment categories from Crime Junkie Podcast. |
| [List Blocks](actions/list-blocks.md) | GET | Retrieves blocks from Crime Junkie Podcast. |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from Crime Junkie Podcast. |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments from Crime Junkie Podcast. |
| [List Content Types](actions/list-content-types.md) | GET | Retrieves content types from Crime Junkie Podcast. |
| [List Dipi Content Categories](actions/list-dipi-content-categories.md) | GET | Retrieves Dipi content categories from Crime Junkie Podcast. |
| [List Dipi Media Categories](actions/list-dipi-media-categories.md) | GET | Retrieves Dipi media categories from Crime Junkie Podcast. |
| [List Fan Club Episodes](actions/list-fan-club-episodes.md) | GET | Retrieves fan club episodes from Crime Junkie Podcast. |
| [List Fan Club Tiers](actions/list-fan-club-tiers.md) | GET | Retrieves fan club tiers from Crime Junkie Podcast. |
| [List Good Tags](actions/list-good-tags.md) | GET | Retrieves good tags from Crime Junkie Podcast. |
| [List Navigation Menus](actions/list-navigation-menus.md) | GET | Retrieves navigation menus from Crime Junkie Podcast. |
| [List Pages](actions/list-pages.md) | GET | Retrieves pages from Crime Junkie Podcast. |
| [List Pattern Categories](actions/list-pattern-categories.md) | GET | Retrieves pattern categories from Crime Junkie Podcast. |
| [List Popup Makers](actions/list-popup-makers.md) | GET | Retrieves popup makers from Crime Junkie Podcast. |
| [List Posts](actions/list-posts.md) | GET | Retrieves posts from Crime Junkie Podcast. |
| [List Project Categories](actions/list-project-categories.md) | GET | Retrieves project categories from Crime Junkie Podcast. |
| [List Project Tags](actions/list-project-tags.md) | GET | Retrieves project tags from Crime Junkie Podcast. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from Crime Junkie Podcast. |
| [List Pruppet Categories](actions/list-pruppet-categories.md) | GET | Retrieves pruppet categories from Crime Junkie Podcast. |
| [List Pruppets](actions/list-pruppets.md) | GET | Retrieves pruppets from Crime Junkie Podcast. |
| [List Recent Episodes](actions/list-recent-episodes.md) | GET | Retrieves recent podcast episodes from Crime Junkie Podcast. |
| [List Statuses](actions/list-statuses.md) | GET | Retrieves statuses from Crime Junkie Podcast. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Crime Junkie Podcast. |
| [List Taxonomies](actions/list-taxonomies.md) | GET | Retrieves taxonomies from Crime Junkie Podcast. |
| [List The Goods](actions/list-the-goods.md) | GET | Retrieves entries from The Goods in Crime Junkie Podcast. |
| [Search Content](actions/search-content.md) | GET | Searches content in Crime Junkie Podcast. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Media](actions/get-media.md) | GET | Retrieves a media item from Crime Junkie Podcast. |
| [List Media](actions/list-media.md) | GET | Retrieves media from Crime Junkie Podcast. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Author](actions/get-author.md) | GET | Retrieves an author from Crime Junkie Podcast. |
| [List Authors](actions/list-authors.md) | GET | Retrieves authors from Crime Junkie Podcast. |

