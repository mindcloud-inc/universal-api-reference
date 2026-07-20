# Expensify: Native API Reference

A consolidated summary of Expensify's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://integrations.expensify.com/Integration-Server/doc/
- **API base URL:** `https://integrations.expensify.com/Integration-Server/`

## Authentication

### Custom

Use the partnerUserID and partnerUserSecret generated from the Expensify integrations page.

### Credentials

- **Partner User ID:** `partnerUserID` · required · The Expensify Integration Server partnerUserID credential.
- **Partner User Secret:** `partnerUserSecret` · required · The Expensify Integration Server partnerUserSecret credential.

[Official authentication documentation](https://integrations.expensify.com/Integration-Server/doc/)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

Responses from this API use JSON. Response data is read from `policyList`.

## Retry behavior

Retry responses with status codes `429`. Wait 10000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Assign Employees To Domain Groups](actions/assign-employees-to-domain-groups.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/) |
| [Create Expense Rule](actions/create-expense-rule.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/#expense-rules-creator) |
| [Create Expenses](actions/create-expenses.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/#expense-creator) |
| [Create Policy](actions/create-policy.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/#policy-creator) |
| [Create Report](actions/create-report.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/#report-creator) |
| [Download Generated File](actions/download-generated-file.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/#downloader) |
| [Dry Run Domain Group Assignment](actions/dry-run-domain-group-assignment.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/) |
| [Dry Run Employee Sync](actions/dry-run-employee-sync.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/) |
| [Dry Run Employee Sync From SFTP](actions/dry-run-employee-sync-from-sftp.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/) |
| [Dry Run Employee Sync From URL](actions/dry-run-employee-sync-from-url.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/) |
| [Dry Run Employee Terminations](actions/dry-run-employee-terminations.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/) |
| [Export Reports](actions/export-reports.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/#report-exporter) |
| [Get Policies](actions/get-policies.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/#policy-getter) |
| [List Domain Cards](actions/list-domain-cards.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/#domain-cards-getter) |
| [List Policies](actions/list-policies.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/#policy-list-getter) |
| [Run Reconciliation Export](actions/run-reconciliation-export.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/#reconciliation) |
| [Sync Additional Policy Memberships](actions/sync-additional-policy-memberships.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/) |
| [Sync Employee Default Tags](actions/sync-employee-default-tags.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/) |
| [Sync Employee Primary Policies](actions/sync-employee-primary-policies.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/) |
| [Sync Employee Roles](actions/sync-employee-roles.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/) |
| [Sync Employees](actions/sync-employees.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/) |
| [Sync Employees From SFTP](actions/sync-employees-from-sftp.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/) |
| [Sync Employees From URL](actions/sync-employees-from-url.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/) |
| [Terminate Employees](actions/terminate-employees.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/employeeUpdater/) |
| [Update Expense Rule](actions/update-expense-rule.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/#expense-rules-updater) |
| [Update Policy Categories](actions/update-policy-categories.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/#policy-updater) |
| [Update Policy Report Fields](actions/update-policy-report-fields.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/#policy-updater) |
| [Update Policy Tags](actions/update-policy-tags.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/#update-tags-nbsp) |
| [Update Report Status](actions/update-report-status.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/#report-status-updater) |
| [Update Tag Approvers](actions/update-tag-approvers.md) | `POST ExpensifyIntegrations` | [docs](https://integrations.expensify.com/Integration-Server/doc/#tag-approvers-updater) |
