# ActivityInfo: Native API Reference

A consolidated summary of ActivityInfo's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://www.activityinfo.org/support/docs/api/index.html
- **API base URL:** `https://www.activityinfo.org`

## Authentication

### Personal API Token

Authenticate requests with an ActivityInfo personal API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.activityinfo.org/support/docs/api/concepts/authentication.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Audit Database](actions/audit-database.md) | `POST /resources/databases/:databaseId/audit` | [docs](https://www.activityinfo.org/support/docs/api/reference/auditDatabase.html) |
| [Download Attachment](actions/download-attachment.md) | `GET /resources/form/:formId/record/:recordId/field/:fieldId/blob/:blobId/:filename` | [docs](https://www.activityinfo.org/support/docs/api/reference/getAttachment.html) |
| [Get Database Billing Account](actions/get-database-billing-account.md) | `GET /resources/databases/:databaseId/billingAccount` | [docs](https://www.activityinfo.org/support/docs/api/reference/getDatabaseBillingAccount.html) |
| [Get Database Problems](actions/get-database-problems.md) | `POST /resources/databases/:databaseId/problems` | [docs](https://www.activityinfo.org/support/docs/api/reference/getDatabaseProblems.html) |
| [Get Database Translations](actions/get-database-translations.md) | `GET /resources/databases/:databaseId/dictionary/:dictionaryId/:language` | [docs](https://www.activityinfo.org/support/docs/api/reference/getTranslations.html) |
| [Get Database Tree](actions/get-database-tree.md) | `GET /resources/databases/:databaseId` | [docs](https://www.activityinfo.org/support/docs/api/reference/getDatabaseTree.html) |
| [Get Form Schema](actions/get-form-schema.md) | `GET /resources/form/:formId/schema` | [docs](https://www.activityinfo.org/support/docs/api/reference/getFormSchema.html) |
| [Get Job Status](actions/get-job-status.md) | `GET /resources/jobs/:jobId` | [docs](https://www.activityinfo.org/support/docs/api/reference/getJobStatus.html) |
| [Get Record](actions/get-record.md) | `GET /resources/form/:formId/record/:recordId` | [docs](https://www.activityinfo.org/support/docs/api/reference/getRecord.html) |
| [Get Record History](actions/get-record-history.md) | `GET /resources/form/:formId/record/:recordId/history` | [docs](https://www.activityinfo.org/support/docs/api/reference/getRecordHistory.html) |
| [Get Report](actions/get-report.md) | `GET /resources/reports/:reportId` | [docs](https://www.activityinfo.org/support/docs/api/reference/getReport.html) |
| [List Billing Account Databases](actions/list-billing-account-databases.md) | `GET /resources/billingAccounts/:accountId/databases` | [docs](https://www.activityinfo.org/support/docs/api/reference/getBillingAccountDatabases.html) |
| [List Billing Account Domains](actions/list-billing-account-domains.md) | `GET /resources/billingAccounts/:accountId/domains` | [docs](https://www.activityinfo.org/support/docs/api/reference/getBillingAccountDomains.html) |
| [List Billing Account Users](actions/list-billing-account-users.md) | `GET /resources/billingAccounts/:accountId/users` | [docs](https://www.activityinfo.org/support/docs/api/reference/getBillingAccountUsers.html) |
| [List Database User Grants On Resource](actions/list-database-user-grants-on-resource.md) | `GET /resources/databases/:databaseId/resources/:resourceId/grants` | [docs](https://www.activityinfo.org/support/docs/api/reference/getDatabaseUserGrantsOnResource.html) |
| [List Database Users](actions/list-database-users.md) | `GET /resources/databases/:databaseId/users` | [docs](https://www.activityinfo.org/support/docs/api/reference/getDatabaseUsers.html) |
| [List Databases](actions/list-databases.md) | `GET /resources/databases` | [docs](https://www.activityinfo.org/support/docs/api/reference/getDatabases.html) |
| [List Form Records](actions/list-form-records.md) | `GET /resources/form/:formId/query` | [docs](https://www.activityinfo.org/support/docs/api/reference/getFormRecords.html) |
| [List Reports](actions/list-reports.md) | `GET /resources/reports` | [docs](https://www.activityinfo.org/support/docs/api/reference/getReports.html) |
| [Ping ActivityInfo](actions/ping-activity-info.md) | `GET /resources/ping` | [docs](https://www.activityinfo.org/support/docs/api/reference/ping.html) |
| [Pivot Query](actions/pivot-query.md) | `POST /resources/query/pivot` | [docs](https://www.activityinfo.org/support/docs/api/reference/pivot.html) |
| [Query Columns](actions/query-columns.md) | `POST /resources/query/columns` | [docs](https://www.activityinfo.org/support/docs/api/reference/queryColumns.html) |
| [Query Form Rows](actions/query-form-rows.md) | `GET /resources/query/v43/form/:formId` | [docs](https://www.activityinfo.org/support/docs/api/reference/queryFormRows.html) |
| [Query Rows](actions/query-rows.md) | `POST /resources/query/rows` | [docs](https://www.activityinfo.org/support/docs/api/reference/queryRows.html) |
| [Search Resources](actions/search-resources.md) | `GET /resources/search` | [docs](https://www.activityinfo.org/support/docs/api/reference/search.html) |
