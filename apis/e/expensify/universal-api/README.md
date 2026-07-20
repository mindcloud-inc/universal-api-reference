# <img src="https://images.mindcloud.co/apps/icons/images-7_1774367621628.png" alt="Expensify logo" width="28" height="28"> Expensify: Universal API

Expensify is an expense management platform. This app wraps the Expensify Integration Server for policy, report, export, and related back-office automation.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/expensify/latest
- **Category:** Commerce / Accounting
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.expensify.com/
- **Vendor API docs:** https://integrations.expensify.com/Integration-Server/doc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Policies](actions/list-policies.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/list-policies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Domain Card

| Action | Method | Description |
| --- | --- | --- |
| [List Domain Cards](actions/list-domain-cards.md) | GET | Retrieves domain cards from Expensify. |

### Downloaded File

| Action | Method | Description |
| --- | --- | --- |
| [Download Generated File](actions/download-generated-file.md) | GET | Retrieves a generated file from Expensify. |

### Employee Sync Preview

| Action | Method | Description |
| --- | --- | --- |
| [Dry Run Domain Group Assignment](actions/dry-run-domain-group-assignment.md) | GET | Retrieves a dry-run domain group assignment result from Expensify. |
| [Dry Run Employee Sync](actions/dry-run-employee-sync.md) | GET | Retrieves a dry-run employee sync result from Expensify. |
| [Dry Run Employee Sync From SFTP](actions/dry-run-employee-sync-from-sftp.md) | GET | Retrieves a dry-run employee sync from SFTP in Expensify. |
| [Dry Run Employee Sync From URL](actions/dry-run-employee-sync-from-url.md) | GET | Retrieves a dry-run employee sync from a URL in Expensify. |
| [Dry Run Employee Terminations](actions/dry-run-employee-terminations.md) | GET | Retrieves a dry-run employee termination result from Expensify. |

### Employee Sync Result

| Action | Method | Description |
| --- | --- | --- |
| [Assign Employees To Domain Groups](actions/assign-employees-to-domain-groups.md) | PUT | Updates employee domain group assignments in Expensify. |
| [Sync Additional Policy Memberships](actions/sync-additional-policy-memberships.md) | PUT | Updates additional policy memberships in Expensify. |
| [Sync Employee Default Tags](actions/sync-employee-default-tags.md) | PUT | Updates employee default tags in Expensify. |
| [Sync Employee Primary Policies](actions/sync-employee-primary-policies.md) | PUT | Updates employee primary policies in Expensify. |
| [Sync Employee Roles](actions/sync-employee-roles.md) | PUT | Updates employee roles in Expensify. |
| [Sync Employees](actions/sync-employees.md) | PUT | Updates employees in Expensify. |
| [Sync Employees From SFTP](actions/sync-employees-from-sftp.md) | PUT | Updates employees in Expensify from SFTP. |
| [Sync Employees From URL](actions/sync-employees-from-url.md) | PUT | Updates employees in Expensify from a URL. |
| [Terminate Employees](actions/terminate-employees.md) | PUT | Updates employee terminations in Expensify. |

### Expense

| Action | Method | Description |
| --- | --- | --- |
| [Create Expenses](actions/create-expenses.md) | POST | Creates new expenses in Expensify. |

### Expense Rule

| Action | Method | Description |
| --- | --- | --- |
| [Create Expense Rule](actions/create-expense-rule.md) | POST | Creates a new expense rule in Expensify. |
| [Update Expense Rule](actions/update-expense-rule.md) | PUT | Updates an existing expense rule in Expensify. |

### Generated File

| Action | Method | Description |
| --- | --- | --- |
| [Export Reports](actions/export-reports.md) | GET | Retrieves exported reports from Expensify. |

### Policy

| Action | Method | Description |
| --- | --- | --- |
| [Create Policy](actions/create-policy.md) | POST | Creates a new policy in Expensify. |
| [List Policies](actions/list-policies.md) | GET | Retrieves policies from Expensify. |

### Policy Category

| Action | Method | Description |
| --- | --- | --- |
| [Update Policy Categories](actions/update-policy-categories.md) | PUT | Updates policy categories in Expensify. |

### Policy Details

| Action | Method | Description |
| --- | --- | --- |
| [Get Policies](actions/get-policies.md) | GET | Retrieves specific policies from Expensify. |

### Policy Report Field

| Action | Method | Description |
| --- | --- | --- |
| [Update Policy Report Fields](actions/update-policy-report-fields.md) | PUT | Updates policy report fields in Expensify. |

### Policy Tag

| Action | Method | Description |
| --- | --- | --- |
| [Update Policy Tags](actions/update-policy-tags.md) | PUT | Updates policy tags in Expensify. |

### Reconciliation File

| Action | Method | Description |
| --- | --- | --- |
| [Run Reconciliation Export](actions/run-reconciliation-export.md) | GET | Retrieves a reconciliation export from Expensify. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Create Report](actions/create-report.md) | POST | Creates a new report in Expensify. |

### Report Status

| Action | Method | Description |
| --- | --- | --- |
| [Update Report Status](actions/update-report-status.md) | PUT | Updates a report status in Expensify. |

### Tag Approver

| Action | Method | Description |
| --- | --- | --- |
| [Update Tag Approvers](actions/update-tag-approvers.md) | PUT | Updates tag approvers in Expensify. |

