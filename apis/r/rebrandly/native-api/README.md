# Rebrandly: Native API Reference

A consolidated summary of Rebrandly's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developers.rebrandly.com/
- **API base URL:** `https://api.rebrandly.com/v1`

## Authentication

### API Key

Connect with a Rebrandly API key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developers.rebrandly.com/docs/api-key-authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `apikey` | query | `string` | no | Maps the Rebrandly API key credential to the shared apikey parameter. |

## Pagination

Use `limit` in the query string to set the page size (default 25; accepted range 1–25). Use `last` in the query string as the pagination cursor.

## Sorting

Set the sort field with `orderBy` in the query string. Set the direction separately with `orderDir`. Use `asc` for ascending order and `desc` for descending order. Multiple sort fields can be combined.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Attach Tag To Link](actions/attach-tag-to-link.md) | `POST /links/:lid/tags/:tid` | [docs](https://developers.rebrandly.com/docs/attaching-a-tag) |
| [Count Domains](actions/count-domains.md) | `GET /domains/count` | [docs](https://developers.rebrandly.com/docs/counting-your-domains) |
| [Count Links](actions/count-links.md) | `GET /links/count` | [docs](https://developers.rebrandly.com/docs/counting-your-links) |
| [Count Tags](actions/count-tags.md) | `GET /tags/count` | [docs](https://developers.rebrandly.com/docs/counting-your-tags) |
| [Create Link](actions/create-link.md) | `POST /links` | [docs](https://developers.rebrandly.com/docs/create-a-new-link) |
| [Create Preset](actions/create-preset.md) | `POST https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/presets` | [docs](https://developers.rebrandly.com/docs/creating-a-preset-1) |
| [Create Query Parameter](actions/create-query-parameter.md) | `POST https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/params` | [docs](https://developers.rebrandly.com/docs/creating-query-parameters) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://developers.rebrandly.com/docs/creating-a-new-tag) |
| [Delete Link](actions/delete-link.md) | `DELETE /links/:id` | [docs](https://developers.rebrandly.com/docs/delete-a-link) |
| [Delete Preset](actions/delete-preset.md) | `DELETE https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/presets/:presetId` | [docs](https://developers.rebrandly.com/docs/delete-a-preset) |
| [Delete Query Parameter](actions/delete-query-parameter.md) | `DELETE https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/params/:paramId` | [docs](https://developers.rebrandly.com/docs/delete-a-query-parameter) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/:id` | [docs](https://developers.rebrandly.com/docs/deleting-a-tag) |
| [Detach Tag From Link](actions/detach-tag-from-link.md) | `DELETE /links/:lid/tags/:tid` | [docs](https://developers.rebrandly.com/docs/detaching-a-tag) |
| [Get Account Details](actions/get-account-details.md) | `GET /account` | [docs](https://developers.rebrandly.com/docs/getting-account-details) |
| [Get Domain Details](actions/get-domain-details.md) | `GET /domains/:id` | [docs](https://developers.rebrandly.com/docs/getting-single-domain-details) |
| [Get Link Details](actions/get-link-details.md) | `GET /links/:id` | [docs](https://developers.rebrandly.com/docs/get-link-details) |
| [Get Link OpenGraph](actions/get-link-open-graph.md) | `GET /links/:id/opengraph` | [docs](https://developers.rebrandly.com/docs/managing-opengraph-metadata-for-links) |
| [Get Tag Details](actions/get-tag-details.md) | `GET /tags/:id` | [docs](https://developers.rebrandly.com/docs/getting-tag-details) |
| [List Domains](actions/list-domains.md) | `GET /domains` | [docs](https://developers.rebrandly.com/docs/listing-your-domains-collection) |
| [List Links](actions/list-links.md) | `GET /links` | [docs](https://developers.rebrandly.com/docs/list-links) |
| [List Presets](actions/list-presets.md) | `GET https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/presets` | [docs](https://developers.rebrandly.com/docs/getting-presets-list) |
| [List Query Parameters](actions/list-query-parameters.md) | `GET https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/params` | [docs](https://developers.rebrandly.com/docs/getting-query-parameters) |
| [List Scripts](actions/list-scripts.md) | `GET /scripts` | [docs](https://developers.rebrandly.com/docs/listing-your-scripts) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://developers.rebrandly.com/docs/listing-your-tags) |
| [List Templates](actions/list-templates.md) | `GET https://templating.rebrandly.com/v1/url/querystring/templates` | [docs](https://developers.rebrandly.com/docs/templates) |
| [List Traffic Rules](actions/list-traffic-rules.md) | `GET /links/:id/rules` | [docs](https://developers.rebrandly.com/docs/advanced-link-options) |
| [Populate Preset](actions/populate-preset.md) | `POST https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/presets/:presetId` | [docs](https://developers.rebrandly.com/docs/updating-a-preset) |
| [Update Link](actions/update-link.md) | `POST /links/:id` | [docs](https://developers.rebrandly.com/docs/update-a-link) |
| [Update Query Parameter](actions/update-query-parameter.md) | `POST https://templating.rebrandly.com/v1/url/querystring/templates/:templateId/params/:paramId` | [docs](https://developers.rebrandly.com/docs/updating-a-query-parameter) |
| [Update Tag](actions/update-tag.md) | `POST /tags/:id` | [docs](https://developers.rebrandly.com/docs/updating-a-tag) |
