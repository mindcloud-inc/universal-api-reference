# Sales Cookie: Native API Reference

A consolidated summary of Sales Cookie's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls
- **API base URL:** `https://salescookie.com/app`

## Authentication

### API key

Use your Sales Cookie workspace API key for OData and REST API access.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-ApiKey: <apiKey>
```

[Official authentication documentation](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `value`.

## Pagination

Use `$top` in the query string to set the page size. Use `$skip` in the query string as the record offset; numbering starts at 0.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add User To Team](actions/add-user-to-team.md) | `POST /Api/CreateTeamMember` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-programmatically-add-or-remove-users-from-teams) |
| [Create Or Update Team](actions/create-or-update-team.md) | `POST /Api/SetTeam` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-programmatically-create-or-update-teams) |
| [Create Or Update User](actions/create-or-update-user.md) | `POST /Api/SetUser` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-programmatically-create-or-update-users) |
| [Create Transaction](actions/create-transaction.md) | `POST /Api/CreateTransaction` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-use-the-simplified-transaction-import-rest-api) |
| [Get Custom Properties](actions/get-custom-properties.md) | `GET /Api/GetCustomProperties` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-programmatically-retrieve-or-set-custom-variables) |
| [Import Transactions](actions/import-transactions.md) | `POST /Api/ImportData` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-use-the-full-transaction-import-rest-api) |
| [List Alerts](actions/list-alerts.md) | `GET /odata/:apiKey/Alert` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Announcements](actions/list-announcements.md) | `GET /odata/:apiKey/Announcement` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Calculation Commissions](actions/list-calculation-commissions.md) | `GET /odata/:apiKey/CalculationCommission` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Calculation Credits](actions/list-calculation-credits.md) | `GET /odata/:apiKey/CalculationCredit` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Calculation Results](actions/list-calculation-results.md) | `GET /odata/:apiKey/CalculationResult` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Calculations](actions/list-calculations.md) | `GET /odata/:apiKey/Calculation?$top=1` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Catalog Entries](actions/list-catalog-entries.md) | `GET /odata/:apiKey/CatalogEntry` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Custom Variables](actions/list-custom-variables.md) | `GET /odata/:apiKey/CustomVariable` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Event Logs](actions/list-event-logs.md) | `GET /odata/:apiKey/EventLog` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Plan Enrollments](actions/list-plan-enrollments.md) | `GET /odata/:apiKey/PlanEnrollment` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Plan Roles](actions/list-plan-roles.md) | `GET /odata/:apiKey/PlanRole` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Plans](actions/list-plans.md) | `GET /odata/:apiKey/Plan` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Reports](actions/list-reports.md) | `GET /odata/:apiKey/Report` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Survey Results](actions/list-survey-results.md) | `GET /odata/:apiKey/SurveyResult` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Surveys](actions/list-surveys.md) | `GET /odata/:apiKey/Survey` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Team Aliases](actions/list-team-aliases.md) | `GET /odata/:apiKey/TeamAlias` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Team Members](actions/list-team-members.md) | `GET /odata/:apiKey/TeamMember` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Teams](actions/list-teams.md) | `GET /odata/:apiKey/Team` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Transactions](actions/list-transactions.md) | `GET /odata/:apiKey/Transaction` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List User Aliases](actions/list-user-aliases.md) | `GET /odata/:apiKey/UserAlias` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Users](actions/list-users.md) | `GET /odata/:apiKey/SystemUser` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Workspace Roles](actions/list-workspace-roles.md) | `GET /odata/:apiKey/WorkspaceRole` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [List Workspace Settings](actions/list-workspace-settings.md) | `GET /odata/:apiKey/WorkspaceSetting` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls) |
| [Prepare Full Transaction Import](actions/prepare-full-transaction-import.md) | `POST /Api/PrepareImport` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-use-the-full-transaction-import-rest-api) |
| [Remove User From Team](actions/remove-user-from-team.md) | `POST /Api/DeleteTeamMember` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-programmatically-add-or-remove-users-from-teams) |
| [Set Custom Properties](actions/set-custom-properties.md) | `POST /Api/SetCustomProperties` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-programmatically-retrieve-or-set-custom-variables) |
| [Upload Transactions Csv](actions/upload-transactions-csv.md) | `POST /Api/UploadTransactions` | [docs](https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-use-the-csv-upload-api) |
