# ActivityInfo: Universal API

ActivityInfo is an information management platform for monitoring and evaluation, reporting, case management, and data collection workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/activityInfo/latest
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.activityinfo.org
- **Vendor API docs:** https://www.activityinfo.org/support/docs/api/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Ping ActivityInfo](actions/ping-activity-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/activityInfo/latest/actions/ping-activity-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Download Attachment](actions/download-attachment.md) | GET | Downloads an attachment from an ActivityInfo record. |

### Audit Entry

| Action | Method | Description |
| --- | --- | --- |
| [Audit Database](actions/audit-database.md) | GET | Retrieves audit entries for an ActivityInfo database. |

### Billing Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Database Billing Account](actions/get-database-billing-account.md) | GET | Retrieves a database's billing account from ActivityInfo. |

### Billing Account Database

| Action | Method | Description |
| --- | --- | --- |
| [List Billing Account Databases](actions/list-billing-account-databases.md) | GET | Retrieves databases for an ActivityInfo billing account. |

### Billing Account Domain

| Action | Method | Description |
| --- | --- | --- |
| [List Billing Account Domains](actions/list-billing-account-domains.md) | GET | Retrieves domains for an ActivityInfo billing account. |

### Billing Account User

| Action | Method | Description |
| --- | --- | --- |
| [List Billing Account Users](actions/list-billing-account-users.md) | GET | Retrieves users for an ActivityInfo billing account. |

### Database

| Action | Method | Description |
| --- | --- | --- |
| [List Databases](actions/list-databases.md) | GET | Retrieves available databases from your ActivityInfo account. |

### Database Problem

| Action | Method | Description |
| --- | --- | --- |
| [Get Database Problems](actions/get-database-problems.md) | GET | Retrieves reported database problems from ActivityInfo. |

### Database Resource Grant

| Action | Method | Description |
| --- | --- | --- |
| [List Database User Grants On Resource](actions/list-database-user-grants-on-resource.md) | GET | Retrieves user grants for an ActivityInfo database resource. |

### Database Tree

| Action | Method | Description |
| --- | --- | --- |
| [Get Database Tree](actions/get-database-tree.md) | GET | Retrieves a database tree from ActivityInfo. |

### Database User

| Action | Method | Description |
| --- | --- | --- |
| [List Database Users](actions/list-database-users.md) | GET | Retrieves users for a specific ActivityInfo database. |

### Form Record

| Action | Method | Description |
| --- | --- | --- |
| [List Form Records](actions/list-form-records.md) | GET | Retrieves records from a specific ActivityInfo form. |

### Form Row

| Action | Method | Description |
| --- | --- | --- |
| [Query Form Rows](actions/query-form-rows.md) | GET | Queries rows for a specific ActivityInfo form. |

### Form Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Schema](actions/get-form-schema.md) | GET | Retrieves a form schema from ActivityInfo. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Job Status](actions/get-job-status.md) | GET | Retrieves a job's status from ActivityInfo. |

### Ping

| Action | Method | Description |
| --- | --- | --- |
| [Ping ActivityInfo](actions/ping-activity-info.md) | GET | Checks whether the ActivityInfo API is reachable. |

### Pivot Result

| Action | Method | Description |
| --- | --- | --- |
| [Pivot Query](actions/pivot-query.md) | GET | Retrieves pivot query results from ActivityInfo. |

### Query Column

| Action | Method | Description |
| --- | --- | --- |
| [Query Columns](actions/query-columns.md) | GET | Queries column data from ActivityInfo form sources. |

### Query Row

| Action | Method | Description |
| --- | --- | --- |
| [Query Rows](actions/query-rows.md) | GET | Queries rows from ActivityInfo form data. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from an ActivityInfo form. |

### Record History

| Action | Method | Description |
| --- | --- | --- |
| [Get Record History](actions/get-record-history.md) | GET | Retrieves a record's history from ActivityInfo. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Report](actions/get-report.md) | GET | Retrieves a specific report from ActivityInfo. |
| [List Reports](actions/list-reports.md) | GET | Retrieves available reports from your ActivityInfo account. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Resources](actions/search-resources.md) | GET | Finds resources in ActivityInfo by search query. |

### Translation Dictionary

| Action | Method | Description |
| --- | --- | --- |
| [Get Database Translations](actions/get-database-translations.md) | GET | Retrieves ActivityInfo translations by dictionary and language. |

