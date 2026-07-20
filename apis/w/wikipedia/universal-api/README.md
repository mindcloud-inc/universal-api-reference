# <img src="https://images.mindcloud.co/apps/icons/wikipedia-logo_1775763607556.png" alt="Wikipedia logo" width="28" height="28"> Wikipedia: Universal API

Public Wikipedia data access through Wikimedia's MediaWiki Action API and REST API, including search, page content, revisions, categories, and discovery endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wikipedia/latest
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.wikipedia.org/
- **Vendor API docs:** https://www.mediawiki.org/wiki/API:Main_page

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Pages](actions/search-pages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wikipedia/latest/actions/search-pages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Categories](actions/get-page-categories.md) | GET | Retrieves categories for a Wikipedia page. |
| [List All Categories](actions/list-all-categories.md) | GET | Lists all article categories in Wikipedia. |
| [List Category Members](actions/list-category-members.md) | GET | Lists pages in a Wikipedia category. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Expand Templates](actions/expand-templates.md) | GET | Expands templates in Wikipedia wikitext content. |
| [Get Page Templates](actions/get-page-templates.md) | GET | Retrieves templates from a Wikipedia page. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Compare Revisions](actions/compare-revisions.md) | GET | Compares two revisions of a Wikipedia page. |
| [Geo Search Pages](actions/geo-search-pages.md) | GET | Finds pages in Wikipedia by nearby coordinates. |
| [Get Page Coordinates](actions/get-page-coordinates.md) | GET | Retrieves coordinates from a Wikipedia page. |
| [Get Page Extract](actions/get-page-extract.md) | GET | Retrieves a page extract from Wikipedia. |
| [Get Page Images](actions/get-page-images.md) | GET | Retrieves images from a Wikipedia page. |
| [Get Page Info](actions/get-page-info.md) | GET | Retrieves detailed page metadata from Wikipedia. |
| [Get Page Language Links](actions/get-page-language-links.md) | GET | Retrieves language links for a Wikipedia page. |
| [Get Page Links](actions/get-page-links.md) | GET | Retrieves links from a Wikipedia page. |
| [Get Page Properties](actions/get-page-properties.md) | GET | Retrieves properties from a Wikipedia page. |
| [Get Page Redirects](actions/get-page-redirects.md) | GET | Retrieves redirects for a Wikipedia page. |
| [Get Page Revisions](actions/get-page-revisions.md) | GET | Retrieves revisions for a Wikipedia page. |
| [Get Random Pages](actions/get-random-pages.md) | GET | Retrieves random encyclopedia pages from Wikipedia. |
| [List All Images](actions/list-all-images.md) | GET | Lists available image files in Wikipedia. |
| [List All Pages](actions/list-all-pages.md) | GET | Lists pages in Wikipedia by title order. |
| [List All Redirects](actions/list-all-redirects.md) | GET | Lists all page redirects in Wikipedia. |
| [List Backlinks](actions/list-backlinks.md) | GET | Lists Wikipedia pages that link to a page. |
| [List Embedded In](actions/list-embedded-in.md) | GET | Lists pages in Wikipedia that embed a page. |
| [List External URL Usage](actions/list-external-url-usage.md) | GET | Lists Wikipedia pages that use an external URL. |
| [List Page Property Names](actions/list-page-property-names.md) | GET | Lists page property names in Wikipedia. |
| [List Pages With Property](actions/list-pages-with-property.md) | GET | Lists Wikipedia pages with a page property. |
| [List Query Page Results](actions/list-query-page-results.md) | GET | Lists results from a Wikipedia query page. |
| [List Recent Changes](actions/list-recent-changes.md) | GET | Lists recent page changes in Wikipedia. |
| [Parse Page](actions/parse-page.md) | GET | Parses a Wikipedia page into HTML content. |
| [Prefix Search Pages](actions/prefix-search-pages.md) | GET | Finds pages in Wikipedia by title prefix. |
| [Search Pages](actions/search-pages.md) | GET | Finds pages in Wikipedia by search query. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List All Users](actions/list-all-users.md) | GET | Lists all user accounts in Wikipedia. |
| [List User Contributions](actions/list-user-contributions.md) | GET | Lists contributions by a Wikipedia user. |

