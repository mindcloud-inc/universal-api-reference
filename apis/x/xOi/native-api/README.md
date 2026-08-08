# XOi: Native API Reference

A consolidated summary of XOi's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://integration-docs.xoi.io/
- **API base URL:** `https://gql-jobs-external.xoi.io/graphql`

## Authentication

### API Key and Secret

Exchange an XOi API key and secret for a 60-minute access token.

### Credentials

- **API Key:** `apiKey` · required · API key issued by XOi for your sandbox integration.
- **API Secret:** `apiSecret` · required · API secret issued by XOi for your sandbox integration.

Send these headers with each API request:

```http
Authorization: <custom.token>
```

[Official authentication documentation](https://integration-docs.xoi.io/guides/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `variables.limit` in the request body to set the page size (default 100; accepted range 1–1000). Use `variables.nextToken` in the request body as the pagination cursor; numbering starts at 0.

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | `POST https://api-users-external.xoi.io/prod/token` | [docs](https://integration-docs.xoi.io/guides/authentication/) |
| [Create Job](actions/create-job.md) | `POST https://gql-jobs-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/jobs/#creating-a-job) |
| [Create Knowledge Base Share Link](actions/create-knowledge-base-share-link.md) | `POST https://gql-share-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/share/) |
| [Create Multi-Job Share Link](actions/create-multi-job-share-link.md) | `POST https://gql-share-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/share/) |
| [Create Share Link](actions/create-share-link.md) | `POST https://gql-share-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/share/) |
| [Delete Job](actions/delete-job.md) | `POST https://gql-jobs-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/jobs/#deleting-a-job) |
| [Get Content](actions/get-content.md) | `POST https://gql-content-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/content/) |
| [Get Content Media URLs](actions/get-content-media-urls.md) | `POST https://gql-content-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/enhanced_content_api/) |
| [Get Groups](actions/get-groups.md) | `POST https://gql-users-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/users/) |
| [Get Job](actions/get-job.md) | `POST https://gql-jobs-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/jobs/#retrieving-a-job) |
| [Get Job ID by External ID](actions/get-job-id-by-external-id.md) | `POST https://gql-jobs-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/schemas/jobs/#getjobidbyexternalidinput) |
| [Get Job IDs](actions/get-job-ids.md) | `POST https://gql-jobs-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/jobs/) |
| [Get Job Summary](actions/get-job-summary.md) | `POST https://gql-jobs-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/jobs/) |
| [Get Live Call Data](actions/get-live-call-data.md) | `POST https://gql-live-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/live/) |
| [Get User](actions/get-user.md) | `POST https://gql-users-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/users/) |
| [Get Users by Email](actions/get-users-by-email.md) | `POST https://gql-users-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/users/) |
| [Get Workflow Job Summary](actions/get-workflow-job-summary.md) | `POST https://gql-jobs-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/schemas/jobs/#getjobsummaryinput) |
| [Get Workflow Reporting Data](actions/get-workflow-reporting-data.md) | `GET https://api-jobs-external.xoi.io/prod/reporting-data/job/:jobId/workflow-job/:workflowJobId` | [docs](https://integration-docs.xoi.io/guides/reporting/) |
| [List Content Webhook History](actions/list-content-webhook-history.md) | `POST https://gql-content-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/content/) |
| [List Documentation](actions/list-documentation.md) | `POST https://gql-jobs-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/jobs/) |
| [List Documentation by Date Range](actions/list-documentation-by-date-range.md) | `POST https://gql-jobs-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/schemas/jobs/#listdocumentationinput) |
| [List Jobs](actions/list-jobs.md) | `POST https://gql-jobs-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/jobs/#getting-a-list-of-jobs) |
| [List Jobs by Customer Name](actions/list-jobs-by-customer-name.md) | `POST https://gql-jobs-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/jobs/#getting-a-list-of-jobs) |
| [List Jobs by Date Range](actions/list-jobs-by-date-range.md) | `POST https://gql-jobs-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/schemas/jobs/#listjobsinput) |
| [List Jobs by Job Location](actions/list-jobs-by-job-location.md) | `POST https://gql-jobs-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/jobs/#getting-a-list-of-jobs) |
| [List Jobs by Work Order](actions/list-jobs-by-work-order.md) | `POST https://gql-jobs-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/jobs/#getting-a-list-of-jobs) |
| [List Jobs Webhook History](actions/list-jobs-webhook-history.md) | `POST https://gql-jobs-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/jobs/) |
| [List Users](actions/list-users.md) | `POST https://gql-users-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/users/) |
| [Prepare Live Call](actions/prepare-live-call.md) | `POST https://gql-live-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/live/) |
| [Search Knowledge Base](actions/search-knowledge-base.md) | `POST https://gql-content-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/content/) |
| [Update Job](actions/update-job.md) | `POST https://gql-jobs-external.xoi.io/graphql` | [docs](https://integration-docs.xoi.io/guides/jobs/#updating-a-job) |
