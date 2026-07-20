# Jobicy: Native API Reference

A consolidated summary of Jobicy's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://jobicy.com/jobs-rss-feed
- **API base URL:** `https://jobicy.com/api/v2`

## Authentication

### No Authentication

Jobicy's public jobs feed does not require account signup, API keys, or OAuth.

This API does not require request authentication.

[Official authentication documentation](https://jobicy.com/jobs-rss-feed)

## API conventions

Shared parameters:

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `geo` | query | `string` | no | Filter jobs by Jobicy region slug such as usa, canada, europe, latam, or apac. |
| `industry` | query | `string` | no | Filter jobs by Jobicy category slug such as engineering, devops, or supporting. |
| `tag` | query | `string` | no | Search jobs by keyword across title and description. |

Responses from this API use JSON. Response data is read from `jobs`.

## Pagination

Use `count` in the query string to set the page size (default 20; accepted range 1–100).

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Accounting and Finance Remote Jobs](actions/list-accounting-and-finance-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Admin Support Remote Jobs](actions/list-admin-support-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List APAC Remote Jobs](actions/list-apac-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Australia Remote Jobs](actions/list-australia-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Brazil Remote Jobs](actions/list-brazil-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Business Remote Jobs](actions/list-business-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Canada Remote Jobs](actions/list-canada-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Copywriting Remote Jobs](actions/list-copywriting-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Customer Support Remote Jobs](actions/list-customer-support-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Data Science Remote Jobs](actions/list-data-science-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Design and Multimedia Remote Jobs](actions/list-design-and-multimedia-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Education Remote Jobs](actions/list-education-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Engineering Remote Jobs](actions/list-engineering-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Europe Remote Jobs](actions/list-europe-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Germany Remote Jobs](actions/list-germany-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Healthcare Remote Jobs](actions/list-healthcare-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List HR Remote Jobs](actions/list-hr-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List LATAM Remote Jobs](actions/list-latam-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Legal Remote Jobs](actions/list-legal-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Marketing Remote Jobs](actions/list-marketing-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Remote Jobs](actions/list-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Remote Jobs by Category](actions/list-remote-jobs-by-category.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Remote Jobs by Region](actions/list-remote-jobs-by-region.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Remote Jobs by Region and Category](actions/list-remote-jobs-by-region-and-category.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Sales Remote Jobs](actions/list-sales-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Software Development Remote Jobs](actions/list-software-development-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List UK Remote Jobs](actions/list-uk-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List USA Remote Jobs](actions/list-usa-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [List Web and App Design Remote Jobs](actions/list-web-and-app-design-remote-jobs.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
| [Search Remote Jobs by Keyword](actions/search-remote-jobs-by-keyword.md) | `GET /remote-jobs` | [docs](https://jobicy.com/jobs-rss-feed) |
