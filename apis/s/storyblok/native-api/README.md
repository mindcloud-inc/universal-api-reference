# Storyblok: Native API Reference

A consolidated summary of Storyblok's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://www.storyblok.com/docs/api/content-delivery/v2
- **API base URL:** `https://api.storyblok.com/v2/cdn`

## Authentication

### Preview API Token

Use a Storyblok preview API token sent as the `token` query parameter.

### Credentials

- **Preview API Token:** `token` · required · The Storyblok Preview API token used for Content Delivery API requests.
- **Space ID:** `spaceId` · required · The numeric Storyblok Space ID used for Storyblok UI resource links.

[Official authentication documentation](https://www.storyblok.com/docs/api/content-delivery/v2/getting-started/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (default 25). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Filter Stories](actions/filter-stories.md) | `GET /stories` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/stories/retrieve-multiple-stories) |
| [Get Current Space](actions/get-current-space.md) | `GET /spaces/me` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/spaces/retrieve-current-space) |
| [Get Datasource](actions/get-datasource.md) | `GET /datasource/:datasourceId` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/datasources/retrieve-a-single-datasource) |
| [Get Link by UUID](actions/get-link-by-path.md) | `GET /links/:linkId` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/links/the-link-object) |
| [Get Signed Asset URL](actions/get-signed-asset-url.md) | `GET /assets/me` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/assets/retrieve-signed-url) |
| [Get Story by Slug](actions/get-story-by-slug.md) | `GET /stories/:storyId` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/stories/retrieve-a-single-story) |
| [Get Story by UUID](actions/get-story-by-uuid.md) | `GET /stories/:storyId` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/stories/retrieve-a-single-story) |
| [Get Story from Release](actions/get-story-from-release.md) | `GET /stories/:storyId` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/stories/examples/retrieving-a-story-from-a-specific-release) |
| [List Datasource Entries](actions/list-datasource-entries.md) | `GET /datasource_entries` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/datasource-entries/retrieve-multiple-datasource-entries) |
| [List Datasources](actions/list-datasources.md) | `GET /datasources` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/datasources/retrieve-multiple-datasources) |
| [List Links](actions/list-links.md) | `GET /links` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/links/retrieve-multiple-links) |
| [List Links in Folder](actions/list-links-in-folder.md) | `GET /links` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/links/retrieve-multiple-links) |
| [List Stories](actions/list-stories.md) | `GET /stories` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/stories/retrieve-multiple-stories) |
| [List Stories by Content Type](actions/list-stories-by-content-type.md) | `GET /stories` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/stories/retrieve-multiple-stories) |
| [List Stories by Language](actions/list-stories-by-language.md) | `GET /stories` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/stories/examples/retrieving-stories-in-a-particular-language) |
| [List Stories by Tag](actions/list-stories-by-tag.md) | `GET /stories` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/stories/retrieve-multiple-stories) |
| [List Stories by UUIDs](actions/list-stories-by-uui-ds.md) | `GET /stories` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/stories/retrieve-multiple-stories) |
| [List Stories in Folder](actions/list-stories-in-folder.md) | `GET /stories` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/stories/examples/retrieving-stories-from-a-folder) |
| [List Stories in Workflow Stage](actions/list-stories-in-workflow-stage.md) | `GET /stories` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/stories/retrieve-multiple-stories) |
| [List Stories with Resolved Relations](actions/list-stories-with-resolved-relations.md) | `GET /stories` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/stories/examples/retrieving-stories-with-resolved-relations) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/tags/retrieve-multiple-tags) |
| [Search Stories](actions/search-stories.md) | `GET /stories` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/stories/retrieve-multiple-stories) |
| [Sort Stories](actions/sort-stories.md) | `GET /stories` | [docs](https://www.storyblok.com/docs/api/content-delivery/v2/stories/examples/sorting-by-story-object-property) |
