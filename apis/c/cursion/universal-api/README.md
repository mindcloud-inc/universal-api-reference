# <img src="https://images.mindcloud.co/apps/icons/cursion-icon_1775657900780.png" alt="Cursion logo" width="28" height="28"> Cursion: Universal API

Cursion is a website QA and performance monitoring platform for sites, pages, scans, tests, issues, schedules, alerts, reports, cases, and flow runs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cursion/latest
- **Category:** IT Operations / Observability
- **Actions:** 37
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cursion.dev
- **Vendor API docs:** https://docs.cursion.dev

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Sites](actions/list-sites.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cursion/latest/actions/list-sites?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (37)

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [Create Alert](actions/create-alert.md) | POST |  |
| [Delete Alert](actions/delete-alert.md) | DELETE | Deletes an existing alert from Cursion. |
| [Get Alert](actions/get-alert.md) | GET | Retrieves an existing alert from Cursion. |
| [List Alerts](actions/list-alerts.md) | GET | Retrieves a list of alerts from Cursion. |

### Issue

| Action | Method | Description |
| --- | --- | --- |
| [Create Issue](actions/create-issue.md) | POST |  |
| [Delete Issue](actions/delete-issue.md) | DELETE | Deletes an existing issue from Cursion. |
| [Generate Issue](actions/generate-issue.md) | POST | Generates an issue from trigger data in Cursion. |
| [Get Issue](actions/get-issue.md) | GET | Retrieves an existing issue from Cursion. |
| [List Issues](actions/list-issues.md) | GET | Retrieves a list of issues from Cursion. |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | POST | Creates a new page in Cursion. |
| [Delete Page](actions/delete-page.md) | DELETE | Deletes an existing page from Cursion. |
| [Delete Pages](actions/delete-pages.md) | DELETE | Deletes multiple existing pages from Cursion. |
| [Get Page](actions/get-page.md) | GET | Retrieves an existing page from Cursion. |
| [List Pages](actions/list-pages.md) | GET | Retrieves a list of pages from Cursion. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Create Report](actions/create-report.md) | POST |  |
| [Delete Report](actions/delete-report.md) | DELETE | Deletes an existing report from Cursion. |
| [Get Report](actions/get-report.md) | GET | Retrieves an existing report from Cursion. |
| [List Reports](actions/list-reports.md) | GET | Retrieves a list of reports from Cursion. |

### Scan

| Action | Method | Description |
| --- | --- | --- |
| [Create Scan](actions/create-scan.md) | POST | Creates a new scan in Cursion. |
| [Delete Scan](actions/delete-scan.md) | DELETE | Deletes an existing scan from Cursion. |
| [Get Lean Scan](actions/get-lean-scan.md) | GET | Retrieves abbreviated scan details from Cursion. |
| [Get Scan](actions/get-scan.md) | GET | Retrieves an existing scan from Cursion. |
| [List Scans](actions/list-scans.md) | GET | Retrieves a list of scans from Cursion. |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Create Schedule](actions/create-schedule.md) | POST |  |
| [Delete Schedule](actions/delete-schedule.md) | DELETE | Deletes an existing schedule from Cursion. |
| [Get Schedule](actions/get-schedule.md) | GET | Retrieves an existing schedule from Cursion. |
| [List Schedules](actions/list-schedules.md) | GET | Retrieves a list of schedules from Cursion. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Create Site](actions/create-site.md) | POST | Creates a new site in Cursion. |
| [Delete Site](actions/delete-site.md) | DELETE | Deletes an existing site from Cursion. |
| [Delete Sites](actions/delete-sites.md) | DELETE | Deletes multiple existing sites from Cursion. |
| [Get Site](actions/get-site.md) | GET | Retrieves an existing site from Cursion. |
| [List Sites](actions/list-sites.md) | GET | Retrieves a list of sites from Cursion. |

### Test

| Action | Method | Description |
| --- | --- | --- |
| [Create Test](actions/create-test.md) | POST | Creates a new test in Cursion. |
| [Delete Test](actions/delete-test.md) | DELETE | Deletes an existing test from Cursion. |
| [Get Lean Test](actions/get-lean-test.md) | GET | Retrieves abbreviated test details from Cursion. |
| [Get Test](actions/get-test.md) | GET | Retrieves an existing test from Cursion. |
| [List Tests](actions/list-tests.md) | GET | Retrieves a list of tests from Cursion. |

