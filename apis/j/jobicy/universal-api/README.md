# <img src="https://images.mindcloud.co/apps/icons/jobicy_1776437748624.png" alt="Jobicy logo" width="28" height="28"> Jobicy: Universal API

Public Jobicy app for reading the latest remote job listings, searching by keyword, and browsing curated regional and category-specific job feeds from Jobicy's official public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/jobicy/latest
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://jobicy.com
- **Vendor API docs:** https://jobicy.com/jobs-rss-feed

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounting and Finance Remote Jobs](actions/list-accounting-and-finance-remote-jobs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jobicy/latest/actions/list-accounting-and-finance-remote-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Job Posting

| Action | Method | Description |
| --- | --- | --- |
| [List Canada Remote Jobs](actions/list-canada-remote-jobs.md) | GET |  |
| [List Remote Jobs](actions/list-remote-jobs.md) | GET |  |
| [List Remote Jobs by Region](actions/list-remote-jobs-by-region.md) | GET |  |
| [Search Remote Jobs by Keyword](actions/search-remote-jobs-by-keyword.md) | GET |  |

### Job Postings

| Action | Method | Description |
| --- | --- | --- |
| [List Accounting and Finance Remote Jobs](actions/list-accounting-and-finance-remote-jobs.md) | GET |  |
| [List Admin Support Remote Jobs](actions/list-admin-support-remote-jobs.md) | GET |  |
| [List APAC Remote Jobs](actions/list-apac-remote-jobs.md) | GET |  |
| [List Australia Remote Jobs](actions/list-australia-remote-jobs.md) | GET |  |
| [List Brazil Remote Jobs](actions/list-brazil-remote-jobs.md) | GET |  |
| [List Business Remote Jobs](actions/list-business-remote-jobs.md) | GET |  |
| [List Copywriting Remote Jobs](actions/list-copywriting-remote-jobs.md) | GET |  |
| [List Customer Support Remote Jobs](actions/list-customer-support-remote-jobs.md) | GET |  |
| [List Data Science Remote Jobs](actions/list-data-science-remote-jobs.md) | GET |  |
| [List Design and Multimedia Remote Jobs](actions/list-design-and-multimedia-remote-jobs.md) | GET |  |
| [List Education Remote Jobs](actions/list-education-remote-jobs.md) | GET |  |
| [List Engineering Remote Jobs](actions/list-engineering-remote-jobs.md) | GET |  |
| [List Europe Remote Jobs](actions/list-europe-remote-jobs.md) | GET |  |
| [List Germany Remote Jobs](actions/list-germany-remote-jobs.md) | GET |  |
| [List Healthcare Remote Jobs](actions/list-healthcare-remote-jobs.md) | GET |  |
| [List HR Remote Jobs](actions/list-hr-remote-jobs.md) | GET |  |
| [List LATAM Remote Jobs](actions/list-latam-remote-jobs.md) | GET |  |
| [List Legal Remote Jobs](actions/list-legal-remote-jobs.md) | GET |  |
| [List Marketing Remote Jobs](actions/list-marketing-remote-jobs.md) | GET |  |
| [List Remote Jobs by Category](actions/list-remote-jobs-by-category.md) | GET |  |
| [List Remote Jobs by Region and Category](actions/list-remote-jobs-by-region-and-category.md) | GET |  |
| [List Sales Remote Jobs](actions/list-sales-remote-jobs.md) | GET |  |
| [List Software Development Remote Jobs](actions/list-software-development-remote-jobs.md) | GET |  |
| [List UK Remote Jobs](actions/list-uk-remote-jobs.md) | GET |  |
| [List USA Remote Jobs](actions/list-usa-remote-jobs.md) | GET |  |
| [List Web and App Design Remote Jobs](actions/list-web-and-app-design-remote-jobs.md) | GET |  |

