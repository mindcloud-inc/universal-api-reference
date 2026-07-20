# Wikipedia: Native API Reference

A consolidated summary of Wikipedia's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://www.mediawiki.org/wiki/API:Main_page
- **API base URL:** `https://en.wikipedia.org`

## Authentication

### No Authentication

Wikipedia public endpoints do not require credentials for the read-only actions in this app.

This API does not require request authentication.

[Official authentication documentation](https://www.mediawiki.org/wiki/API:Main_page)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `User-Agent` | `MindCloud Wikipedia App/1.0` |

## Retry behavior

Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Compare Revisions](actions/compare-revisions.md) | `GET /w/api.php?action=compare&format=json` | [docs](https://www.mediawiki.org/wiki/API:Compare) |
| [Expand Templates](actions/expand-templates.md) | `GET /w/api.php?action=expandtemplates&prop=wikitext&format=json` | [docs](https://www.mediawiki.org/wiki/API:Expandtemplates) |
| [Geo Search Pages](actions/geo-search-pages.md) | `GET /w/api.php?action=query&list=geosearch&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:Geosearch) |
| [Get Page Categories](actions/get-page-categories.md) | `GET /w/api.php?action=query&prop=categories&format=json&formatversion=2&redirects=1` | [docs](https://www.mediawiki.org/wiki/API:Categories) |
| [Get Page Coordinates](actions/get-page-coordinates.md) | `GET /w/api.php?action=query&prop=coordinates&format=json&formatversion=2&redirects=1` | [docs](https://www.mediawiki.org/wiki/API:Coordinates) |
| [Get Page Extract](actions/get-page-extract.md) | `GET /w/api.php?action=query&prop=extracts&explaintext=1&format=json&formatversion=2&redirects=1` | [docs](https://www.mediawiki.org/wiki/API:Extracts) |
| [Get Page Images](actions/get-page-images.md) | `GET /w/api.php?action=query&prop=images&format=json&formatversion=2&redirects=1` | [docs](https://www.mediawiki.org/wiki/API:Images) |
| [Get Page Info](actions/get-page-info.md) | `GET /w/api.php?action=query&prop=info&inprop=url&format=json&formatversion=2&redirects=1` | [docs](https://www.mediawiki.org/wiki/API:Info) |
| [Get Page Language Links](actions/get-page-language-links.md) | `GET /w/api.php?action=query&prop=langlinks&format=json&formatversion=2&redirects=1` | [docs](https://www.mediawiki.org/wiki/API:Langlinks) |
| [Get Page Links](actions/get-page-links.md) | `GET /w/api.php?action=query&prop=links&format=json&formatversion=2&redirects=1` | [docs](https://www.mediawiki.org/wiki/API:Links) |
| [Get Page Properties](actions/get-page-properties.md) | `GET /w/api.php?action=query&prop=pageprops&format=json&formatversion=2&redirects=1` | [docs](https://www.mediawiki.org/wiki/API:Pageprops) |
| [Get Page Redirects](actions/get-page-redirects.md) | `GET /w/api.php?action=query&prop=redirects&format=json&formatversion=2&redirects=1` | [docs](https://www.mediawiki.org/wiki/API:Redirects) |
| [Get Page Revisions](actions/get-page-revisions.md) | `GET /w/api.php?action=query&prop=revisions&rvprop=ids\|timestamp\|user\|comment\|size&format=json&formatversion=2&redirects=1` | [docs](https://www.mediawiki.org/wiki/API:Revisions) |
| [Get Page Templates](actions/get-page-templates.md) | `GET /w/api.php?action=query&prop=templates&format=json&formatversion=2&redirects=1` | [docs](https://www.mediawiki.org/wiki/API:Templates) |
| [Get Random Pages](actions/get-random-pages.md) | `GET /w/api.php?action=query&list=random&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:Random) |
| [List All Categories](actions/list-all-categories.md) | `GET /w/api.php?action=query&list=allcategories&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:Allcategories) |
| [List All Images](actions/list-all-images.md) | `GET /w/api.php?action=query&list=allimages&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:Allimages) |
| [List All Pages](actions/list-all-pages.md) | `GET /w/api.php?action=query&list=allpages&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:Allpages) |
| [List All Redirects](actions/list-all-redirects.md) | `GET /w/api.php?action=query&list=allredirects&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:Allredirects) |
| [List All Users](actions/list-all-users.md) | `GET /w/api.php?action=query&list=allusers&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:Allusers) |
| [List Backlinks](actions/list-backlinks.md) | `GET /w/api.php?action=query&list=backlinks&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:Backlinks) |
| [List Category Members](actions/list-category-members.md) | `GET /w/api.php?action=query&list=categorymembers&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:Categorymembers) |
| [List Embedded In](actions/list-embedded-in.md) | `GET /w/api.php?action=query&list=embeddedin&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:Embeddedin) |
| [List External URL Usage](actions/list-external-url-usage.md) | `GET /w/api.php?action=query&list=exturlusage&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:Exturlusage) |
| [List Page Property Names](actions/list-page-property-names.md) | `GET /w/api.php?action=query&list=pagepropnames&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:Pagepropnames) |
| [List Pages With Property](actions/list-pages-with-property.md) | `GET /w/api.php?action=query&list=pageswithprop&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:Pageswithprop) |
| [List Query Page Results](actions/list-query-page-results.md) | `GET /w/api.php?action=query&list=querypage&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:Querypage) |
| [List Recent Changes](actions/list-recent-changes.md) | `GET /w/api.php?action=query&list=recentchanges&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:RecentChanges) |
| [List User Contributions](actions/list-user-contributions.md) | `GET /w/api.php?action=query&list=usercontribs&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:Usercontribs) |
| [Parse Page](actions/parse-page.md) | `GET /w/api.php?action=parse&prop=text\|categories\|links&format=json` | [docs](https://www.mediawiki.org/wiki/API:Parsing_wikitext) |
| [Prefix Search Pages](actions/prefix-search-pages.md) | `GET /w/api.php?action=query&list=prefixsearch&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:Prefixsearch) |
| [Search Pages](actions/search-pages.md) | `GET /w/api.php?action=query&list=search&format=json&formatversion=2` | [docs](https://www.mediawiki.org/wiki/API:Search) |
