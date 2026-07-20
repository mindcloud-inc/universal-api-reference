# Socket: Native API Reference

A consolidated summary of Socket's API configuration and 91 documented operations, with links to official documentation.

- **Official docs:** https://docs.socket.dev/reference
- **OpenAPI specification:** https://api.socket.dev/v0/openapi
- **API base URL:** `https://api.socket.dev/v0`

## Authentication

### API Token

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.socket.dev/docs/api-keys)

## Endpoints (91 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Associate Repository Label](actions/associate-repository-label.md) | `POST /orgs/:org_slug/repos/labels/:label_id/associate` | [docs](https://docs.socket.dev/reference/associateorgrepolabel) |
| [Calculate Settings](actions/calculate-settings.md) | `POST /settings` | [docs](https://docs.socket.dev/reference/postsettings) |
| [Compare License Data with Policy](actions/compare-license-data-with-policy.md) | `POST /license-policy` | [docs](https://docs.socket.dev/reference/licensepolicy) |
| [Create API Token](actions/create-api-token.md) | `POST /orgs/:org_slug/api-tokens` | [docs](https://docs.socket.dev/reference/postapitoken) |
| [Create Dependencies Snapshot](actions/create-dependencies-snapshot.md) | `POST /dependencies/upload` | [docs](https://docs.socket.dev/reference/createdependenciessnapshot) |
| [Create Diff Scan from IDs](actions/create-diff-scan-from-ids.md) | `POST /orgs/:org_slug/diff-scans/from-ids` | [docs](https://docs.socket.dev/reference/createorgdiffscanfromids) |
| [Create Diff Scan from Repository](actions/create-diff-scan-from-repository.md) | `POST /orgs/:org_slug/diff-scans/from-repo/:repo_slug` | [docs](https://docs.socket.dev/reference/createorgrepodiff) |
| [Create Full Scan](actions/create-full-scan.md) | `POST /orgs/:org_slug/full-scans` | [docs](https://docs.socket.dev/reference/createorgfullscan) |
| [Create Full Scan from Archive](actions/create-full-scan-from-archive.md) | `POST /orgs/:org_slug/full-scans/archive` | [docs](https://docs.socket.dev/reference/createorgfullscanarchive) |
| [Create Repository](actions/create-repository.md) | `POST /orgs/:org_slug/repos` | [docs](https://docs.socket.dev/reference/createorgrepo) |
| [Create Repository Label](actions/create-repository-label.md) | `POST /orgs/:org_slug/repos/labels` | [docs](https://docs.socket.dev/reference/createorgrepolabel) |
| [Create Webhook](actions/create-webhook.md) | `POST /orgs/:org_slug/webhooks` | [docs](https://docs.socket.dev/reference/createorgwebhook) |
| [Delete Alert Triage](actions/delete-alert-triage.md) | `DELETE /orgs/:org_slug/triage/alerts/:uuid` | [docs](https://docs.socket.dev/reference/deleteorgalerttriage) |
| [Delete Diff Scan](actions/delete-diff-scan.md) | `DELETE /orgs/:org_slug/diff-scans/:diff_scan_id` | [docs](https://docs.socket.dev/reference/deleteorgdiffscan) |
| [Delete Full Scan](actions/delete-full-scan.md) | `DELETE /orgs/:org_slug/full-scans/:full_scan_id` | [docs](https://docs.socket.dev/reference/deleteorgfullscan) |
| [Delete Report](actions/delete-report.md) | `DELETE /report/delete/:id` | [docs](https://docs.socket.dev/reference/deletereport) |
| [Delete Repository](actions/delete-repository.md) | `DELETE /orgs/:org_slug/repos/:repo_slug` | [docs](https://docs.socket.dev/reference/deleteorgrepo) |
| [Delete Repository Label](actions/delete-repository-label.md) | `DELETE /orgs/:org_slug/repos/labels/:label_id` | [docs](https://docs.socket.dev/reference/deleteorgrepolabel) |
| [Delete Repository Label Setting](actions/delete-repository-label-setting.md) | `DELETE /orgs/:org_slug/repos/labels/:label_id/label-setting` | [docs](https://docs.socket.dev/reference/deleteorgrepolabelsetting) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /orgs/:org_slug/webhooks/:webhook_id` | [docs](https://docs.socket.dev/reference/deleteorgwebhook) |
| [Disassociate Repository Label](actions/disassociate-repository-label.md) | `POST /orgs/:org_slug/repos/labels/:label_id/disassociate` | [docs](https://docs.socket.dev/reference/disassociateorgrepolabel) |
| [Download Full Scan Files Tar](actions/download-full-scan-files-tar.md) | `GET /orgs/:org_slug/full-scans/:full_scan_id/files/tar` | [docs](https://docs.socket.dev/reference/downloadorgfullscanfilesastar) |
| [Export CycloneDX SBOM](actions/export-cyclonedx-sbom.md) | `GET /orgs/:org_slug/export/cdx/:id` | [docs](https://docs.socket.dev/reference/exportcdx) |
| [Export Full Scan CSV](actions/export-full-scan-csv.md) | `POST /orgs/:org_slug/full-scans/:full_scan_id/format/csv` | [docs](https://docs.socket.dev/reference/getorgfullscancsv) |
| [Export Full Scan PDF](actions/export-full-scan-pdf.md) | `POST /orgs/:org_slug/full-scans/:full_scan_id/format/pdf` | [docs](https://docs.socket.dev/reference/getorgfullscanpdf) |
| [Export OpenVEX](actions/export-openvex.md) | `GET /orgs/:org_slug/export/openvex/:id` | [docs](https://docs.socket.dev/reference/exportopenvex) |
| [Export SPDX SBOM](actions/export-spdx-sbom.md) | `GET /orgs/:org_slug/export/spdx/:id` | [docs](https://docs.socket.dev/reference/exportspdx) |
| [Fetch Fixes](actions/fetch-fixes.md) | `GET /orgs/:org_slug/fixes` | [docs](https://docs.socket.dev/reference/fetch-fixes) |
| [Get Alert Types Metadata](actions/get-alert-types-metadata.md) | `POST /alert-types` | [docs](https://docs.socket.dev/reference/alerttypes) |
| [Get Audit Log Events](actions/get-audit-log-events.md) | `GET /orgs/:org_slug/audit-log` | [docs](https://docs.socket.dev/reference/getauditlogevents) |
| [Get Diff Scan](actions/get-diff-scan.md) | `GET /orgs/:org_slug/diff-scans/:diff_scan_id` | [docs](https://docs.socket.dev/reference/getdiffscanbyid) |
| [Get Diff Scan GFM](actions/get-diff-scan-gfm.md) | `GET /orgs/:org_slug/diff-scans/:diff_scan_id/gfm` | [docs](https://docs.socket.dev/reference/getdiffscangfm) |
| [Get Full Scan Diff](actions/get-full-scan-diff.md) | `GET /orgs/:org_slug/full-scans/diff` | [docs](https://docs.socket.dev/reference/getorgdiffscan) |
| [Get Full Scan Diff GFM](actions/get-full-scan-diff-gfm.md) | `GET /orgs/:org_slug/full-scans/diff/gfm` | [docs](https://docs.socket.dev/reference/getorgfullscandiffgfm) |
| [Get Full Scan Metadata](actions/get-full-scan-metadata.md) | `GET /orgs/:org_slug/full-scans/:full_scan_id/metadata` | [docs](https://docs.socket.dev/reference/getorgfullscanmetadata) |
| [Get Integration Events](actions/get-integration-events.md) | `GET /orgs/:org_slug/settings/integrations/:integration_id/events` | [docs](https://docs.socket.dev/reference/getintegrationevents) |
| [Get Issues by Package](actions/get-issues-by-package.md) | `GET /npm/:package/:version/issues` | [docs](https://docs.socket.dev/reference/getissuesbynpmpackage) |
| [Get License Metadata](actions/get-license-metadata.md) | `POST /license-metadata` | [docs](https://docs.socket.dev/reference/licensemetadata) |
| [Get License Policy](actions/get-license-policy.md) | `GET /orgs/:org_slug/settings/license-policy/view` | [docs](https://docs.socket.dev/reference/viewlicensepolicy) |
| [Get Organization Analytics](actions/get-organization-analytics.md) | `GET /analytics/org/:filter` | [docs](https://docs.socket.dev/reference/getorganalytics) |
| [Get Organization License Policy](actions/get-organization-license-policy.md) | `GET /orgs/:org_slug/settings/license-policy` | [docs](https://docs.socket.dev/reference/getorglicensepolicy) |
| [Get Packages by PURL](actions/get-packages-by-purl.md) | `POST /purl` | [docs](https://docs.socket.dev/reference/batchpackagefetch) |
| [Get Packages by PURL for Organization](actions/get-packages-by-purl-for-organization.md) | `POST /orgs/:org_slug/purl` | [docs](https://docs.socket.dev/reference/batchpackagefetchbyorg) |
| [Get Quota](actions/get-quota.md) | `GET /quota` | [docs](https://docs.socket.dev/reference/getquota) |
| [Get Report Supported Files](actions/get-report-supported-files.md) | `GET /report/supported` | [docs](https://docs.socket.dev/reference/getreportsupportedfiles) |
| [Get Repository](actions/get-repository.md) | `GET /orgs/:org_slug/repos/:repo_slug` | [docs](https://docs.socket.dev/reference/getorgrepo) |
| [Get Repository Analytics](actions/get-repository-analytics.md) | `GET /analytics/repo/:name/:filter` | [docs](https://docs.socket.dev/reference/getrepoanalytics) |
| [Get Repository Label](actions/get-repository-label.md) | `GET /orgs/:org_slug/repos/labels/:label_id` | [docs](https://docs.socket.dev/reference/getorgrepolabel) |
| [Get Repository Label Setting](actions/get-repository-label-setting.md) | `GET /orgs/:org_slug/repos/labels/:label_id/label-setting` | [docs](https://docs.socket.dev/reference/getorgrepolabelsetting) |
| [Get Score by Package](actions/get-score-by-package.md) | `GET /npm/:package/:version/score` | [docs](https://docs.socket.dev/reference/getscorebynpmpackage) |
| [Get Security Policy](actions/get-security-policy.md) | `GET /orgs/:org_slug/settings/security-policy` | [docs](https://docs.socket.dev/reference/getorgsecuritypolicy) |
| [Get Socket Basics Config](actions/get-socket-basics-config.md) | `GET /orgs/:org_slug/settings/socket-basics` | [docs](https://docs.socket.dev/reference/getsocketbasicsconfig) |
| [Get Supported Files](actions/get-supported-files.md) | `GET /orgs/:org_slug/supported-files` | [docs](https://docs.socket.dev/reference/getsupportedfiles) |
| [Get Telemetry Config](actions/get-telemetry-config.md) | `GET /orgs/:org_slug/telemetry/config` | [docs](https://docs.socket.dev/reference/getorgtelemetryconfig) |
| [Get Threat Feed Items](actions/get-threat-feed-items.md) | `GET /threat-feed` | [docs](https://docs.socket.dev/reference/getthreatfeeditems) |
| [Get Threat Feed Items for Organization](actions/get-threat-feed-items-for-organization.md) | `GET /orgs/:org_slug/threat-feed` | [docs](https://docs.socket.dev/reference/getorgthreatfeeditems) |
| [Get Trend of Historical Alerts](actions/get-trend-of-historical-alerts.md) | `GET /orgs/:org_slug/historical/alerts/trend` | [docs](https://docs.socket.dev/reference/historicalalertstrend) |
| [Get Trend of Historical Dependencies](actions/get-trend-of-historical-dependencies.md) | `GET /orgs/:org_slug/historical/dependencies/trend` | [docs](https://docs.socket.dev/reference/historicaldependenciestrend) |
| [Get Webhook](actions/get-webhook.md) | `GET /orgs/:org_slug/webhooks/:webhook_id` | [docs](https://docs.socket.dev/reference/getorgwebhook) |
| [List Alert Full Scans](actions/list-alert-full-scans.md) | `GET /orgs/:org_slug/alert-full-scan-search` | [docs](https://docs.socket.dev/reference/alertfullscans) |
| [List Alert Triage](actions/list-alert-triage.md) | `GET /orgs/:org_slug/triage/alerts` | [docs](https://docs.socket.dev/reference/getorgtriage) |
| [List Alerts](actions/list-alerts.md) | `GET /orgs/:org_slug/alerts` | [docs](https://docs.socket.dev/reference/alertslist) |
| [List API Tokens](actions/list-api-tokens.md) | `GET /orgs/:org_slug/api-tokens` | [docs](https://docs.socket.dev/reference/getapitokens) |
| [List Diff Scans](actions/list-diff-scans.md) | `GET /orgs/:org_slug/diff-scans` | [docs](https://docs.socket.dev/reference/listorgdiffscans) |
| [List Full Scans](actions/list-full-scans.md) | `GET /orgs/:org_slug/full-scans` | [docs](https://docs.socket.dev/reference/getorgfullscanlist) |
| [List GitHub Repositories](actions/list-git-hub-repositories.md) | `GET /repo/list` | [docs](https://docs.socket.dev/reference/getrepolist) |
| [List Historical Alerts](actions/list-historical-alerts.md) | `GET /orgs/:org_slug/historical/alerts` | [docs](https://docs.socket.dev/reference/historicalalertslist) |
| [List Historical Snapshots](actions/list-historical-snapshots.md) | `GET /orgs/:org_slug/historical/snapshots` | [docs](https://docs.socket.dev/reference/historicalsnapshotslist) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://docs.socket.dev/reference/getorganizations) |
| [List Reports](actions/list-reports.md) | `GET /report/list` | [docs](https://docs.socket.dev/reference/getreportlist) |
| [List Repositories](actions/list-repositories.md) | `GET /orgs/:org_slug/repos` | [docs](https://docs.socket.dev/reference/getorgrepolist) |
| [List Repository Labels](actions/list-repository-labels.md) | `GET /orgs/:org_slug/repos/labels` | [docs](https://docs.socket.dev/reference/getorgrepolabellist) |
| [List Webhooks](actions/list-webhooks.md) | `GET /orgs/:org_slug/webhooks` | [docs](https://docs.socket.dev/reference/getorgwebhookslist) |
| [Rescan Full Scan](actions/rescan-full-scan.md) | `POST /orgs/:org_slug/full-scans/:full_scan_id/rescan` | [docs](https://docs.socket.dev/reference/rescanorgfullscan) |
| [Revoke API Token](actions/revoke-api-token.md) | `POST /orgs/:org_slug/api-tokens/revoke` | [docs](https://docs.socket.dev/reference/postapitokensrevoke) |
| [Rotate API Token](actions/rotate-api-token.md) | `POST /orgs/:org_slug/api-tokens/rotate` | [docs](https://docs.socket.dev/reference/postapitokensrotate) |
| [Saturate License Policy](actions/saturate-license-policy.md) | `POST /saturate-license-policy` | [docs](https://docs.socket.dev/reference/saturatelicensepolicy) |
| [Search Dependencies](actions/search-dependencies.md) | `POST /dependencies/search` | [docs](https://docs.socket.dev/reference/searchdependencies) |
| [Start Historical Data Snapshot Job](actions/start-historical-data-snapshot-job.md) | `POST /orgs/:org_slug/historical/snapshots` | [docs](https://docs.socket.dev/reference/historicalsnapshotsstart) |
| [Stream Full Scan](actions/stream-full-scan.md) | `GET /orgs/:org_slug/full-scans/:full_scan_id` | [docs](https://docs.socket.dev/reference/getorgfullscan) |
| [Update Alert Triage](actions/update-alert-triage.md) | `POST /orgs/:org_slug/triage/alerts` | [docs](https://docs.socket.dev/reference/updateorgalerttriage) |
| [Update API Token](actions/update-api-token.md) | `POST /orgs/:org_slug/api-tokens/update` | [docs](https://docs.socket.dev/reference/postapitokenupdate) |
| [Update License Policy](actions/update-license-policy.md) | `POST /orgs/:org_slug/settings/license-policy` | [docs](https://docs.socket.dev/reference/updateorglicensepolicy) |
| [Update Repository](actions/update-repository.md) | `POST /orgs/:org_slug/repos/:repo_slug` | [docs](https://docs.socket.dev/reference/updateorgrepo) |
| [Update Repository Label](actions/update-repository-label.md) | `PUT /orgs/:org_slug/repos/labels/:label_id` | [docs](https://docs.socket.dev/reference/updateorgrepolabel) |
| [Update Repository Label Setting](actions/update-repository-label-setting.md) | `PUT /orgs/:org_slug/repos/labels/:label_id/label-setting` | [docs](https://docs.socket.dev/reference/updateorgrepolabelsetting) |
| [Update Security Policy](actions/update-security-policy.md) | `POST /orgs/:org_slug/settings/security-policy` | [docs](https://docs.socket.dev/reference/updateorgsecuritypolicy) |
| [Update Telemetry Config](actions/update-telemetry-config.md) | `PUT /orgs/:org_slug/telemetry/config` | [docs](https://docs.socket.dev/reference/updateorgtelemetryconfig) |
| [Update Webhook](actions/update-webhook.md) | `PUT /orgs/:org_slug/webhooks/:webhook_id` | [docs](https://docs.socket.dev/reference/updateorgwebhook) |
| [Upload Report](actions/upload-report.md) | `PUT /report/upload` | [docs](https://docs.socket.dev/reference/createreport) |
| [View Report](actions/view-report.md) | `GET /report/view/:id` | [docs](https://docs.socket.dev/reference/getreport) |
