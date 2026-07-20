# <img src="https://images.mindcloud.co/apps/icons/sales-cookie_1777045658566.png" alt="Sales Cookie logo" width="28" height="28"> Sales Cookie: Universal API

Import transactions and read commission calculations and incentive data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/salesCookie/latest
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://salescookie.com/
- **Vendor API docs:** https://support2.salescookie.com/portal/en/kb/articles/kb-how-can-i-access-sales-incentive-data-using-api-calls

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Calculations](actions/list-calculations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/list-calculations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [List Alerts](actions/list-alerts.md) | GET | Retrieves workspace alerts from Sales Cookie. |

### Announcement

| Action | Method | Description |
| --- | --- | --- |
| [List Announcements](actions/list-announcements.md) | GET | Retrieves workspace announcements from Sales Cookie. |

### Calculation

| Action | Method | Description |
| --- | --- | --- |
| [List Calculations](actions/list-calculations.md) | GET | Retrieves calculation records from Sales Cookie. |

### Calculationcommission

| Action | Method | Description |
| --- | --- | --- |
| [List Calculation Commissions](actions/list-calculation-commissions.md) | GET | Retrieves calculation commissions from Sales Cookie. |

### Calculationcredit

| Action | Method | Description |
| --- | --- | --- |
| [List Calculation Credits](actions/list-calculation-credits.md) | GET | Retrieves calculation credits from Sales Cookie. |

### Calculationresult

| Action | Method | Description |
| --- | --- | --- |
| [List Calculation Results](actions/list-calculation-results.md) | GET | Retrieves calculation results from Sales Cookie. |

### Catalogentry

| Action | Method | Description |
| --- | --- | --- |
| [List Catalog Entries](actions/list-catalog-entries.md) | GET | Retrieves product catalog entries from Sales Cookie. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Properties](actions/get-custom-properties.md) | GET | Retrieves custom properties for a Sales Cookie entity. |
| [List Custom Variables](actions/list-custom-variables.md) | GET | Retrieves custom variables from Sales Cookie. |
| [Set Custom Properties](actions/set-custom-properties.md) | PUT | Replaces custom properties on a Sales Cookie entity. |

### Eventlog

| Action | Method | Description |
| --- | --- | --- |
| [List Event Logs](actions/list-event-logs.md) | GET | Retrieves workspace event logs from Sales Cookie. |

### Import Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Import Transactions](actions/import-transactions.md) | POST | Imports transaction CSV data into Sales Cookie. |
| [Prepare Full Transaction Import](actions/prepare-full-transaction-import.md) | POST | Prepares a transaction import batch in Sales Cookie. |
| [Upload Transactions Csv](actions/upload-transactions-csv.md) | POST | Uploads transaction CSV data to Sales Cookie. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [Add User To Team](actions/add-user-to-team.md) | POST | Adds a user to a team in Sales Cookie. |
| [List Team Members](actions/list-team-members.md) | GET | Retrieves team member records from Sales Cookie. |
| [Remove User From Team](actions/remove-user-from-team.md) | DELETE | Removes a user from a team in Sales Cookie. |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [List Plans](actions/list-plans.md) | GET | Retrieves commission plans from Sales Cookie. |

### Planenrollment

| Action | Method | Description |
| --- | --- | --- |
| [List Plan Enrollments](actions/list-plan-enrollments.md) | GET | Retrieves plan enrollments from Sales Cookie. |

### Planrole

| Action | Method | Description |
| --- | --- | --- |
| [List Plan Roles](actions/list-plan-roles.md) | GET | Retrieves plan roles from Sales Cookie. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [List Reports](actions/list-reports.md) | GET | Retrieves published reports from Sales Cookie. |

### Survey

| Action | Method | Description |
| --- | --- | --- |
| [List Surveys](actions/list-surveys.md) | GET | Retrieves incentive surveys from Sales Cookie. |

### Surveyresult

| Action | Method | Description |
| --- | --- | --- |
| [List Survey Results](actions/list-survey-results.md) | GET | Retrieves survey results from Sales Cookie. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Team](actions/create-or-update-team.md) | PUT | Creates or updates a team in Sales Cookie by name. |
| [List Team Aliases](actions/list-team-aliases.md) | GET | Retrieves team aliases from Sales Cookie. |
| [List Teams](actions/list-teams.md) | GET | Retrieves workspace teams from Sales Cookie. |

### Transactions

| Action | Method | Description |
| --- | --- | --- |
| [Create Transaction](actions/create-transaction.md) | POST | Creates or updates a transaction in Sales Cookie by unique ID. |
| [List Transactions](actions/list-transactions.md) | GET | Retrieves commission transactions from Sales Cookie. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update User](actions/create-or-update-user.md) | PUT | Creates or updates a user in Sales Cookie by email address. |
| [List User Aliases](actions/list-user-aliases.md) | GET | Retrieves user aliases from Sales Cookie. |
| [List Users](actions/list-users.md) | GET | Retrieves workspace users from Sales Cookie. |

### Workspacerole

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Roles](actions/list-workspace-roles.md) | GET | Retrieves workspace roles from Sales Cookie. |

### Workspacesetting

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Settings](actions/list-workspace-settings.md) | GET | Retrieves workspace settings from Sales Cookie. |

