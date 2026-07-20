# <img src="https://images.mindcloud.co/apps/icons/action1-icon_1776869416770.png" alt="Action1 logo" width="28" height="28"> Action1: Universal API

Manage endpoints, deploy patches, run automations, and track vulnerabilities

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/action1/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.action1.com/
- **Vendor API docs:** https://app.action1.com/apidocs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User Settings](actions/get-current-user-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/action1/latest/actions/get-current-user-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Audit Event

| Action | Method | Description |
| --- | --- | --- |
| [List Audit Events](actions/list-audit-events.md) | GET | Retrieves audit trail events from Action1. |

### Automation Instance

| Action | Method | Description |
| --- | --- | --- |
| [List Automation Instances](actions/list-automation-instances.md) | GET | Retrieves automation instances from Action1 for an organization. |

### Automation Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Automation Schedules](actions/list-automation-schedules.md) | GET | Retrieves automation schedules from Action1 for an organization. |

### Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Get Endpoint](actions/get-endpoint.md) | GET | Retrieves a managed endpoint from Action1 by ID. |
| [List Endpoints](actions/list-endpoints.md) | GET | Retrieves managed endpoints from Action1 for an organization. |

### Endpoint Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Endpoint Group](actions/get-endpoint-group.md) | GET | Retrieves an endpoint group from Action1 by ID. |
| [List Endpoint Groups](actions/list-endpoint-groups.md) | GET | Retrieves endpoint groups from Action1 for an organization. |

### Endpoint Group Content

| Action | Method | Description |
| --- | --- | --- |
| [List Endpoint Group Contents](actions/list-endpoint-group-contents.md) | GET | Retrieves endpoint group contents from Action1 by group ID. |

### Endpoint Status

| Action | Method | Description |
| --- | --- | --- |
| [Check Endpoint Status](actions/check-endpoint-status.md) | GET | Retrieves endpoint addition status from Action1 for an organization. |

### Installed Software Row

| Action | Method | Description |
| --- | --- | --- |
| [List Endpoint Installed Software Rows](actions/list-endpoint-installed-software-rows.md) | GET | Retrieves installed software rows from Action1 for a specific endpoint. |
| [List Installed Software Rows](actions/list-installed-software-rows.md) | GET | Retrieves installed software rows from Action1 for an organization. |

### Missing Update

| Action | Method | Description |
| --- | --- | --- |
| [Get Missing Update](actions/get-missing-update.md) | GET | Retrieves available update versions from Action1 for a package. |
| [List Endpoint Missing Updates](actions/list-endpoint-missing-updates.md) | GET | Retrieves missing updates from Action1 for a specific endpoint. |
| [List Missing Updates](actions/list-missing-updates.md) | GET | Retrieves missing updates from Action1 for an organization. |

### Missing Update Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [List Missing Update Version Endpoints](actions/list-missing-update-version-endpoints.md) | GET | Retrieves endpoints missing a specific update version in Action1. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from the current Action1 enterprise. |

### Remediation

| Action | Method | Description |
| --- | --- | --- |
| [List Vulnerability Remediations](actions/list-vulnerability-remediations.md) | GET | Retrieves vulnerability remediation history from Action1. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [List Reports](actions/list-reports.md) | GET | Retrieves all enterprise reports from Action1. |

### Report Row

| Action | Method | Description |
| --- | --- | --- |
| [Get Report Rows](actions/get-report-rows.md) | GET | Retrieves report rows from Action1 for a report. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search](actions/search.md) | GET | Finds Action1 objects in an organization by query. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User Settings](actions/get-current-user-settings.md) | GET | Retrieves current user settings from Action1. |

### Vulnerability

| Action | Method | Description |
| --- | --- | --- |
| [Get Vulnerability](actions/get-vulnerability.md) | GET | Retrieves vulnerability details from Action1 by CVE ID. |
| [List Vulnerabilities](actions/list-vulnerabilities.md) | GET | Retrieves vulnerabilities from Action1 for an organization. |

### Vulnerability Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [List Vulnerability Endpoints](actions/list-vulnerability-endpoints.md) | GET | Retrieves endpoints affected by a vulnerability in Action1. |

