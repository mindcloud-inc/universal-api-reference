# Omniconvert Explore: Native API Reference

A consolidated summary of Omniconvert Explore's API configuration and 12 documented operations, with links to official documentation.

- **Official docs:** https://api.omniconvert.com/docs
- **API base URL:** `https://api.omniconvert.com/v1`

## Authentication

### Custom

Use your Omniconvert legacy V1 API key and the email address for the same dashboard account.

### Credentials

- **API Key:** `apiKey` · required · Legacy V1 API key from the V1 (legacy) tab in Omniconvert API Credentials.
- **API User:** `apiUser` · required · Email address used to sign in to the same Omniconvert account as the V1 key.

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
X-Api-User: <apiUser>
```

[Official authentication documentation](https://api.omniconvert.com/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort-by` in the query string. Set the direction separately with `sort-direction`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (12 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete Segment](actions/delete-segment.md) | `DELETE /segments/:id` | [docs](https://api.omniconvert.com/docs#delete--v1-segments-{id}) |
| [Get Experiment](actions/get-experiment.md) | `GET /experiments/:experimentId` | [docs](https://api.omniconvert.com/docs#get--v1-experiments-{experimentId}) |
| [Get Experiment Stats](actions/get-experiment-stats.md) | `GET /experiments/:experimentId/stats` | [docs](https://api.omniconvert.com/docs#get--v1-experiments-{experimentId}-stats) |
| [Get Segment](actions/get-segment.md) | `GET /segments/:id` | [docs](https://api.omniconvert.com/docs#get--v1-segments-{id}) |
| [Get Website Growth](actions/get-website-growth.md) | `GET /websites/:id/growth` | [docs](https://api.omniconvert.com/docs#get--v1-websites-{id}-growth) |
| [Get Website Stats](actions/get-website-stats.md) | `GET /websites/:websiteId/stats` | [docs](https://api.omniconvert.com/docs#get--v1-websites-{websiteId}-stats) |
| [List Active Experiments](actions/list-active-experiments.md) | `GET /active-experiments` | [docs](https://api.omniconvert.com/docs#get--v1-active-experiments) |
| [List Experiments](actions/list-experiments.md) | `GET /experiments` | [docs](https://api.omniconvert.com/docs#get--v1-experiments) |
| [List Segments](actions/list-segments.md) | `GET /segments` | [docs](https://api.omniconvert.com/docs#get--v1-segments) |
| [List Websites](actions/list-websites.md) | `GET /websites` | [docs](https://api.omniconvert.com/docs#get--v1-websites) |
| [Start or Stop Experiment](actions/start-or-stop-experiment.md) | `POST /experiments/:experimentId/:action` | [docs](https://api.omniconvert.com/docs#post--v1-experiments-{experimentId}-{action}) |
| [Validate Account](actions/validate-account.md) | `GET https://api.omniconvert.com/zapier/validate-account` | [docs](https://api.omniconvert.com/docs#get--zapier-validate-account) |
