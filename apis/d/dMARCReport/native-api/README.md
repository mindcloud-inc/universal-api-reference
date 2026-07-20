# DMARC Report: Native API Reference

A consolidated summary of DMARC Report's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.dmarcreport.com/api/2.0.html
- **API base URL:** `https://api.dmarcreport.com/v2`

## Authentication

### DMARC Report API Token

Use a DMARC Report API token. Requests authenticate with the Authorization header using Token token=<token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.dmarcreport.com/api/2.0.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per` in the query string to set the page size (default 25; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Account Domain](actions/create-account-domain.md) | `POST /accounts/:accountId/domain_accounts.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [Create Domain](actions/create-domain.md) | `POST /accounts/:accountId/domains.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [Delete Account Domain](actions/delete-account-domain.md) | `DELETE /accounts/:accountId/domain_accounts/:id.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [Delete Domain](actions/delete-domain.md) | `DELETE /accounts/:accountId/domains/:id.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [Generate DMARC Record](actions/generate-dmarc-record.md) | `POST /accounts/:accountId/domains/:domainId/generate_dmarc_record.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [Get Account Domain](actions/get-account-domain.md) | `GET /accounts/:accountId/domain_accounts/:id` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [Get Aggregate Report](actions/get-aggregate-report.md) | `GET /accounts/:accountId/domains/:domainId/agg_reports/:id.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [Get Aggregate Report Records](actions/get-aggregate-report-records.md) | `GET /accounts/:accountId/domains/:domainId/agg_reports/records.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [Get Domain](actions/get-domain.md) | `GET /accounts/:accountId/domains/:id.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [Get Forensic Report](actions/get-forensic-report.md) | `GET /accounts/:accountId/domains/:domainId/forensic_reports/:id.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [Get Hosted Services](actions/get-hosted-services.md) | `GET /accounts/:accountId/domains/:domainId/hosted_services.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [Get MTA-STS Report](actions/get-mta-sts-report.md) | `GET /accounts/:accountId/domains/:domainId/mta_sts_reports/:id.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [Get Postmaster Account Record](actions/get-postmaster-account-record.md) | `GET /postmaster_account_records/:id.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [List Account Domains](actions/list-account-domains.md) | `GET /accounts/:accountId/domain_accounts` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [List Aggregate Reports](actions/list-aggregate-reports.md) | `GET /accounts/:accountId/domains/:domainId/agg_reports.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [List All Domains](actions/list-all-domains.md) | `GET /all_domains.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [List Connected Postmaster Accounts](actions/list-connected-postmaster-accounts.md) | `GET /postmaster_account_records/connected.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [List Domains](actions/list-domains.md) | `GET /accounts/:accountId/domains.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [List Forensic Reports](actions/list-forensic-reports.md) | `GET /accounts/:accountId/domains/:domainId/forensic_reports.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [List MTA-STS Failure Details](actions/list-mta-sts-failure-details.md) | `GET /accounts/:accountId/domains/:domainId/mta_sts_reports/mta_failure_details.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [List MTA-STS Reports](actions/list-mta-sts-reports.md) | `GET /accounts/:accountId/domains/:domainId/mta_sts_reports.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [List Postmaster Account Records](actions/list-postmaster-account-records.md) | `GET /postmaster_account_records.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
| [Update Domain](actions/update-domain.md) | `PUT /accounts/:accountId/domains/:id.json` | [docs](https://docs.dmarcreport.com/api/2.0.html) |
