# <img src="https://images.mindcloud.co/apps/icons/images-1_1774550770260.png" alt="Socket logo" width="28" height="28"> Socket: Universal API

Socket: Manage dependencies, scans, alerts, policies, and repositories

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/socket/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 91
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://socket.dev
- **Vendor API docs:** https://docs.socket.dev/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Quota](actions/get-quota.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-quota?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (91)

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [List Alerts](actions/list-alerts.md) | GET | Retrieves latest organization alerts from Socket. |

### Alert Triage

| Action | Method | Description |
| --- | --- | --- |
| [Delete Alert Triage](actions/delete-alert-triage.md) | DELETE | Deletes an existing alert triage rule from Socket. |
| [List Alert Triage](actions/list-alert-triage.md) | GET | Retrieves organization alert triage rules from Socket. |
| [Update Alert Triage](actions/update-alert-triage.md) | PUT | Creates or updates alert triage rules in Socket. |

### Alert Type

| Action | Method | Description |
| --- | --- | --- |
| [Get Alert Types Metadata](actions/get-alert-types-metadata.md) | POST | Retrieves alert type metadata from Socket. |

### Api Token

| Action | Method | Description |
| --- | --- | --- |
| [Create API Token](actions/create-api-token.md) | POST | Creates a new API token in Socket. |
| [List API Tokens](actions/list-api-tokens.md) | GET | Retrieves organization API tokens from Socket. |
| [Revoke API Token](actions/revoke-api-token.md) | DELETE | Revokes an existing API token in Socket. |
| [Rotate API Token](actions/rotate-api-token.md) | PUT | Rotates an existing API token in Socket. |
| [Update API Token](actions/update-api-token.md) | PUT | Updates an existing API token in Socket. |

### Audit Log Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Audit Log Events](actions/get-audit-log-events.md) | GET | Retrieves audit log events from Socket. |

### Dependency

| Action | Method | Description |
| --- | --- | --- |
| [Search Dependencies](actions/search-dependencies.md) | GET | Finds dependencies used in Socket by search criteria. |

### Dependency Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [Create Dependencies Snapshot](actions/create-dependencies-snapshot.md) | POST | Creates a dependency snapshot in Socket. |

### Diff Scan

| Action | Method | Description |
| --- | --- | --- |
| [Create Diff Scan from IDs](actions/create-diff-scan-from-ids.md) | POST | Creates a diff scan in Socket from scan IDs. |
| [Create Diff Scan from Repository](actions/create-diff-scan-from-repository.md) | POST | Creates a diff scan in Socket from a repository. |
| [Delete Diff Scan](actions/delete-diff-scan.md) | DELETE | Deletes an existing diff scan from Socket. |
| [Get Diff Scan](actions/get-diff-scan.md) | GET | Retrieves a diff scan from Socket. |
| [Get Diff Scan GFM](actions/get-diff-scan-gfm.md) | GET | Retrieves a diff scan as GitHub Flavored Markdown from Socket. |
| [List Diff Scans](actions/list-diff-scans.md) | GET | Retrieves organization diff scans from Socket. |

### Export

| Action | Method | Description |
| --- | --- | --- |
| [Export CycloneDX SBOM](actions/export-cyclonedx-sbom.md) | GET | Exports a Socket SBOM in CycloneDX format. |
| [Export OpenVEX](actions/export-openvex.md) | GET | Exports OpenVEX vulnerability data from Socket. |
| [Export SPDX SBOM](actions/export-spdx-sbom.md) | GET | Exports a Socket SBOM in SPDX format. |

### Fix

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Fixes](actions/fetch-fixes.md) | GET | Retrieves available vulnerability fixes from Socket. |

### Full Scan

| Action | Method | Description |
| --- | --- | --- |
| [Create Full Scan](actions/create-full-scan.md) | POST | Creates a new full scan in Socket. |
| [Create Full Scan from Archive](actions/create-full-scan-from-archive.md) | POST | Creates a full scan in Socket from an archive. |
| [Delete Full Scan](actions/delete-full-scan.md) | DELETE | Deletes an existing full scan from Socket. |
| [Download Full Scan Files Tar](actions/download-full-scan-files-tar.md) | GET | Downloads a full scan tarball from Socket. |
| [Export Full Scan CSV](actions/export-full-scan-csv.md) | GET | Exports full scan alerts from Socket as CSV. |
| [Export Full Scan PDF](actions/export-full-scan-pdf.md) | GET | Exports full scan alerts from Socket as PDF. |
| [Get Full Scan Diff](actions/get-full-scan-diff.md) | GET | Retrieves a full scan diff from Socket. |
| [Get Full Scan Diff GFM](actions/get-full-scan-diff-gfm.md) | GET | Retrieves a full scan diff as GitHub Flavored Markdown from Socket. |
| [Get Full Scan Metadata](actions/get-full-scan-metadata.md) | GET | Retrieves full scan metadata from Socket. |
| [List Alert Full Scans](actions/list-alert-full-scans.md) | GET | Retrieves full scans associated with alerts from Socket. |
| [List Full Scans](actions/list-full-scans.md) | GET | Retrieves organization full scans from Socket. |
| [Rescan Full Scan](actions/rescan-full-scan.md) | PUT | Rescans an existing full scan in Socket. |
| [Stream Full Scan](actions/stream-full-scan.md) | GET | Streams full scan artifacts from Socket. |

### Historical Alert

| Action | Method | Description |
| --- | --- | --- |
| [Get Trend of Historical Alerts](actions/get-trend-of-historical-alerts.md) | GET | Retrieves historical alert trends from Socket. |
| [List Historical Alerts](actions/list-historical-alerts.md) | GET | Retrieves historical organization alerts from Socket. |

### Historical Dependency

| Action | Method | Description |
| --- | --- | --- |
| [Get Trend of Historical Dependencies](actions/get-trend-of-historical-dependencies.md) | GET | Retrieves historical dependency trends from Socket. |

### Historical Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [List Historical Snapshots](actions/list-historical-snapshots.md) | GET | Retrieves historical organization snapshots from Socket. |
| [Start Historical Data Snapshot Job](actions/start-historical-data-snapshot-job.md) | POST | Starts a historical data snapshot job in Socket. |

### Integration Event

| Action | Method | Description |
| --- | --- | --- |
| [Get Integration Events](actions/get-integration-events.md) | GET | Retrieves organization integration events from Socket. |

### License Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get License Metadata](actions/get-license-metadata.md) | POST | Retrieves license metadata records from Socket. |

### License Policy

| Action | Method | Description |
| --- | --- | --- |
| [Compare License Data with Policy](actions/compare-license-data-with-policy.md) | PUT | Compares package license data with a Socket policy. |
| [Get License Policy](actions/get-license-policy.md) | GET | Retrieves an organization license policy from Socket. |
| [Get Organization License Policy](actions/get-organization-license-policy.md) | GET | Retrieves a deprecated organization license policy from Socket. |
| [Saturate License Policy](actions/saturate-license-policy.md) | PUT | Retrieves a saturated Socket license policy. |
| [Update License Policy](actions/update-license-policy.md) | PUT | Updates an organization license policy in Socket. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations associated with your Socket token. |

### Organization Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Analytics](actions/get-organization-analytics.md) | GET | Retrieves organization analytics data from Socket. |

### Package

| Action | Method | Description |
| --- | --- | --- |
| [Get Packages by PURL](actions/get-packages-by-purl.md) | GET | Retrieves packages by PURL from Socket. |
| [Get Packages by PURL for Organization](actions/get-packages-by-purl-for-organization.md) | GET | Retrieves packages by PURL for a Socket organization. |

### Package Issue

| Action | Method | Description |
| --- | --- | --- |
| [Get Issues by Package](actions/get-issues-by-package.md) | GET | Retrieves package issue details from Socket. |

### Package Score

| Action | Method | Description |
| --- | --- | --- |
| [Get Score by Package](actions/get-score-by-package.md) | GET | Retrieves a package score from Socket. |

### Quota

| Action | Method | Description |
| --- | --- | --- |
| [Get Quota](actions/get-quota.md) | GET | Retrieves current API quota details from Socket. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Delete Report](actions/delete-report.md) | DELETE | Deletes an existing report from Socket. |
| [Get Report Supported Files](actions/get-report-supported-files.md) | GET | Retrieves supported report files from Socket. |
| [List Reports](actions/list-reports.md) | GET | Retrieves uploaded analysis reports from Socket. |
| [Upload Report](actions/upload-report.md) | POST | Uploads an analysis report to Socket. |
| [View Report](actions/view-report.md) | GET | Retrieves an uploaded report from Socket. |

### Repository

| Action | Method | Description |
| --- | --- | --- |
| [Create Repository](actions/create-repository.md) | POST | Creates a new repository in Socket. |
| [Delete Repository](actions/delete-repository.md) | DELETE | Deletes an existing repository from Socket. |
| [Get Repository](actions/get-repository.md) | GET | Retrieves detailed repository data from Socket. |
| [List GitHub Repositories](actions/list-git-hub-repositories.md) | GET | Retrieves GitHub repositories available in Socket. |
| [List Repositories](actions/list-repositories.md) | GET | Retrieves organization repositories available in Socket. |
| [Update Repository](actions/update-repository.md) | PUT | Updates an existing repository in Socket. |

### Repository Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Repository Analytics](actions/get-repository-analytics.md) | GET | Retrieves repository analytics data from Socket. |

### Repository Label

| Action | Method | Description |
| --- | --- | --- |
| [Associate Repository Label](actions/associate-repository-label.md) | PUT | Associates a repository label with a Socket repository. |
| [Create Repository Label](actions/create-repository-label.md) | POST | Creates a new repository label in Socket. |
| [Delete Repository Label](actions/delete-repository-label.md) | DELETE | Deletes an existing repository label from Socket. |
| [Disassociate Repository Label](actions/disassociate-repository-label.md) | PUT | Disassociates a repository label from a Socket repository. |
| [Get Repository Label](actions/get-repository-label.md) | GET | Retrieves a repository label from Socket. |
| [List Repository Labels](actions/list-repository-labels.md) | GET | Retrieves repository labels configured in Socket. |
| [Update Repository Label](actions/update-repository-label.md) | PUT | Updates an existing repository label in Socket. |

### Repository Label Setting

| Action | Method | Description |
| --- | --- | --- |
| [Delete Repository Label Setting](actions/delete-repository-label-setting.md) | DELETE | Deletes an existing repository label setting from Socket. |
| [Get Repository Label Setting](actions/get-repository-label-setting.md) | GET | Retrieves a repository label setting from Socket. |
| [Update Repository Label Setting](actions/update-repository-label-setting.md) | PUT | Updates an existing repository label setting in Socket. |

### Security Policy

| Action | Method | Description |
| --- | --- | --- |
| [Get Security Policy](actions/get-security-policy.md) | GET | Retrieves an organization security policy from Socket. |
| [Update Security Policy](actions/update-security-policy.md) | PUT | Updates an organization security policy in Socket. |

### Settings

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Settings](actions/calculate-settings.md) | POST | Retrieves current settings for requested Socket organizations. |

### Socket Basics

| Action | Method | Description |
| --- | --- | --- |
| [Get Socket Basics Config](actions/get-socket-basics-config.md) | GET | Retrieves Socket Basics configuration from Socket. |

### Supported Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Supported Files](actions/get-supported-files.md) | GET | Retrieves supported full scan files from Socket. |

### Telemetry Config

| Action | Method | Description |
| --- | --- | --- |
| [Get Telemetry Config](actions/get-telemetry-config.md) | GET | Retrieves an organization telemetry configuration from Socket. |
| [Update Telemetry Config](actions/update-telemetry-config.md) | PUT | Updates an organization telemetry configuration in Socket. |

### Threat Feed

| Action | Method | Description |
| --- | --- | --- |
| [Get Threat Feed Items](actions/get-threat-feed-items.md) | GET | Retrieves deprecated threat feed items from Socket. |
| [Get Threat Feed Items for Organization](actions/get-threat-feed-items-for-organization.md) | GET | Retrieves organization threat feed items from Socket. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Socket. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Socket. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a configured webhook from Socket. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves configured organization webhooks from Socket. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Socket. |

