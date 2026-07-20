# UpGuard: Native API Reference

A consolidated summary of UpGuard's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://cyber-risk.upguard.com/api/docs
- **OpenAPI specification:** https://cyber-risk.upguard.com/api/swagger.json
- **API base URL:** `https://cyber-risk.upguard.com/api/public`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://help.upguard.com/en/articles/8060003-how-to-authenticate-with-your-upguard-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 1000; accepted range 10–2000). Use `page_token` in the query string as the pagination cursor.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `sort_desc`. Use `false` for ascending order and `true` for descending order. Only one sort field is accepted.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Identity Breach Details](actions/get-identity-breach-details.md) | `GET /breach` | [docs](https://cyber-risk.upguard.com/api/docs#operation/identity_breach) |
| [Get Onboarding Request](actions/get-onboarding-request.md) | `GET /onboarding_request` | [docs](https://cyber-risk.upguard.com/api/docs#operation/onboardingRequestGet) |
| [Get Organisation](actions/get-organisation.md) | `GET /organisation` | [docs](https://cyber-risk.upguard.com/api/docs#operation/getOrganisationV1) |
| [Get Portfolio Risk Profile Overview](actions/get-portfolio-risk-profile-overview.md) | `GET /risks/vendors/all` | [docs](https://cyber-risk.upguard.com/api/docs#operation/vendor_risk_overview_params) |
| [Get Risk Details](actions/get-risk-details.md) | `GET /available_risks/risk` | [docs](https://cyber-risk.upguard.com/api/docs#operation/risk) |
| [Get Vendor Details](actions/get-vendor-details.md) | `GET /vendor` | [docs](https://cyber-risk.upguard.com/api/docs#operation/vendor) |
| [Get Vendor Questionnaire Metadata](actions/get-vendor-questionnaire-metadata.md) | `GET /vendor/questionnaire` | [docs](https://cyber-risk.upguard.com/api/docs#operation/questionnaireGet) |
| [Get Vendor Questionnaire Questions And Answers](actions/get-vendor-questionnaire-questions-and-answers.md) | `GET /vendor/questionnaire/answers` | [docs](https://cyber-risk.upguard.com/api/docs#operation/questionnaireAnswers) |
| [List Active Risks](actions/list-active-risks.md) | `GET /risks` | [docs](https://cyber-risk.upguard.com/api/docs#operation/risks) |
| [List Available Risks](actions/list-available-risks.md) | `GET /available_risks/v2` | [docs](https://cyber-risk.upguard.com/api/docs#operation/available_risks_v2) |
| [List Breached Identities](actions/list-breached-identities.md) | `GET /breaches` | [docs](https://cyber-risk.upguard.com/api/docs#operation/breached_identities) |
| [List Domains](actions/list-domains.md) | `GET /domains` | [docs](https://cyber-risk.upguard.com/api/docs#operation/domains) |
| [List IP Ranges](actions/list-ip-ranges.md) | `GET /ranges` | [docs](https://cyber-risk.upguard.com/api/docs#operation/ranges) |
| [List IPs](actions/list-ips.md) | `GET /ips` | [docs](https://cyber-risk.upguard.com/api/docs#operation/ips) |
| [List Labels](actions/list-labels.md) | `GET /labels` | [docs](https://cyber-risk.upguard.com/api/docs#operation/labels) |
| [List Monitored Vendor Risk Changes](actions/list-monitored-vendor-risk-changes.md) | `GET /risks/vendors/diffs` | [docs](https://cyber-risk.upguard.com/api/docs#operation/vendors_risks_diff) |
| [List Monitored Vendors](actions/list-monitored-vendors.md) | `GET /vendors` | [docs](https://cyber-risk.upguard.com/api/docs#operation/vendors) |
| [List Onboarding Requests](actions/list-onboarding-requests.md) | `GET /onboarding_request/list` | [docs](https://cyber-risk.upguard.com/api/docs#operation/onboardingRequestsList) |
| [List Risk Changes](actions/list-risk-changes.md) | `GET /risks/diff` | [docs](https://cyber-risk.upguard.com/api/docs#operation/org_risks_diff) |
| [List Typosquat Domains](actions/list-typosquat-domains.md) | `GET /typosquat` | [docs](https://cyber-risk.upguard.com/api/docs#operation/listTyposquatDomains) |
| [List Vendor Domains](actions/list-vendor-domains.md) | `GET /vendor/domains` | [docs](https://cyber-risk.upguard.com/api/docs#operation/vendor_domains) |
| [List Vendor IPs](actions/list-vendor-ips.md) | `GET /vendor/ips` | [docs](https://cyber-risk.upguard.com/api/docs#operation/vendor_ips) |
| [List Vendor Questionnaires](actions/list-vendor-questionnaires.md) | `GET /vendor/questionnaires/v2` | [docs](https://cyber-risk.upguard.com/api/docs#operation/questionnairesV2) |
| [List Vendor Risks](actions/list-vendor-risks.md) | `GET /risks/vendors` | [docs](https://cyber-risk.upguard.com/api/docs#operation/vendor_risks) |
| [List Vendor Vulnerabilities](actions/list-vendor-vulnerabilities.md) | `GET /vulnerabilities/vendor` | [docs](https://cyber-risk.upguard.com/api/docs#operation/vendor_vulnerabilities) |
| [List Vendors Affected By Risk](actions/list-vendors-affected-by-risk.md) | `GET /risks/vendors_with_risk` | [docs](https://cyber-risk.upguard.com/api/docs#operation/get_vendors_with_risk_params) |
| [List Vulnerabilities](actions/list-vulnerabilities.md) | `GET /vulnerabilities` | [docs](https://cyber-risk.upguard.com/api/docs#operation/org_vulnerabilities) |
| [Retrieve Domain Details](actions/retrieve-domain-details.md) | `GET /domain` | [docs](https://cyber-risk.upguard.com/api/docs#operation/domain_details) |
| [Retrieve IP Details](actions/retrieve-ip-details.md) | `GET /ip` | [docs](https://cyber-risk.upguard.com/api/docs#operation/ip_details) |
| [Retrieve Typosquat Details](actions/retrieve-typosquat-details.md) | `GET /typosquat/details` | [docs](https://cyber-risk.upguard.com/api/docs#operation/typosquat_details) |
| [Retrieve Vendor Domain Details](actions/retrieve-vendor-domain-details.md) | `GET /vendor/domain` | [docs](https://cyber-risk.upguard.com/api/docs#operation/vendor_domain_details) |
| [Retrieve Vendor IP Details](actions/retrieve-vendor-ip-details.md) | `GET /vendor/ip` | [docs](https://cyber-risk.upguard.com/api/docs#operation/vendor_ip_details) |
| [Send Security Questionnaire To Vendor](actions/send-security-questionnaire-to-vendor.md) | `POST /vendor/questionnaire` | [docs](https://cyber-risk.upguard.com/api/docs#operation/sendQuestionnaire) |
| [Start Monitoring Vendor](actions/start-monitoring-vendor.md) | `POST /vendor/monitor` | [docs](https://cyber-risk.upguard.com/api/docs#operation/monitorvendor) |
| [Stop Monitoring Vendor](actions/stop-monitoring-vendor.md) | `POST /vendor/unmonitor` | [docs](https://cyber-risk.upguard.com/api/docs#operation/unmonitorvendor) |
| [Update Domain Labels](actions/update-domain-labels.md) | `PUT /domain/labels` | [docs](https://cyber-risk.upguard.com/api/docs#operation/domain_update_labels) |
| [Update IP Labels](actions/update-ip-labels.md) | `PUT /ip/labels` | [docs](https://cyber-risk.upguard.com/api/docs#operation/ip_update_labels) |
| [Update Vendor Attributes](actions/update-vendor-attributes.md) | `PUT /vendor/attributes` | [docs](https://cyber-risk.upguard.com/api/docs#operation/vendor_update_attributes) |
| [Update Vendor Labels](actions/update-vendor-labels.md) | `PUT /vendor/labels` | [docs](https://cyber-risk.upguard.com/api/docs#operation/vendor_update_labels) |
| [Update Vendor Tier](actions/update-vendor-tier.md) | `PUT /vendor/tier` | [docs](https://cyber-risk.upguard.com/api/docs#operation/vendor_update_tier) |
