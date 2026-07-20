# <img src="https://images.mindcloud.co/apps/icons/dmarc-report-icon-filled-256_1776709742903.png" alt="DMARC Report logo" width="28" height="28"> DMARC Report: Universal API

DMARC Report lets teams monitor DMARC, forensic, MTA-STS, domain, account, and Postmaster reporting data through the DMARC Report API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dMARCReport/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dmarcreport.com/
- **Vendor API docs:** https://docs.dmarcreport.com/api/2.0.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accounts](actions/list-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accessible accounts from DMARC Report. |

### Account Domain

| Action | Method | Description |
| --- | --- | --- |
| [Create Account Domain](actions/create-account-domain.md) | POST | Creates a domain account in DMARC Report. |
| [Delete Account Domain](actions/delete-account-domain.md) | DELETE | Deletes a domain account from DMARC Report. |
| [Get Account Domain](actions/get-account-domain.md) | GET | Retrieves a domain account from DMARC Report. |
| [List Account Domains](actions/list-account-domains.md) | GET | Retrieves domain accounts from a DMARC Report account. |

### Aggregate Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Aggregate Report](actions/get-aggregate-report.md) | GET | Retrieves an aggregate report from DMARC Report. |
| [List Aggregate Reports](actions/list-aggregate-reports.md) | GET | Retrieves aggregate reports from DMARC Report. |

### Aggregate Report Record

| Action | Method | Description |
| --- | --- | --- |
| [Get Aggregate Report Records](actions/get-aggregate-report-records.md) | GET | Retrieves aggregate report records from DMARC Report. |

### Dmarc Record

| Action | Method | Description |
| --- | --- | --- |
| [Generate DMARC Record](actions/generate-dmarc-record.md) | POST | Generates a DMARC record for a domain in DMARC Report. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Create Domain](actions/create-domain.md) | POST | Creates a domain in a DMARC Report account. |
| [Delete Domain](actions/delete-domain.md) | DELETE | Deletes a domain from DMARC Report. |
| [Get Domain](actions/get-domain.md) | GET | Retrieves a domain from DMARC Report. |
| [List All Domains](actions/list-all-domains.md) | GET | Retrieves all domains from DMARC Report. |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from a DMARC Report account. |
| [Update Domain](actions/update-domain.md) | PUT | Updates an existing domain in DMARC Report. |

### Forensic Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Forensic Report](actions/get-forensic-report.md) | GET | Retrieves a forensic report from DMARC Report. |
| [List Forensic Reports](actions/list-forensic-reports.md) | GET | Retrieves forensic reports from DMARC Report. |

### Hosted Service

| Action | Method | Description |
| --- | --- | --- |
| [Get Hosted Services](actions/get-hosted-services.md) | GET | Retrieves hosted service status for a domain in DMARC Report. |

### Mta-sts Failure Detail

| Action | Method | Description |
| --- | --- | --- |
| [List MTA-STS Failure Details](actions/list-mta-sts-failure-details.md) | GET | Retrieves MTA-STS failure details from DMARC Report. |

### Mta-sts Report

| Action | Method | Description |
| --- | --- | --- |
| [Get MTA-STS Report](actions/get-mta-sts-report.md) | GET | Retrieves an MTA-STS report from DMARC Report. |
| [List MTA-STS Reports](actions/list-mta-sts-reports.md) | GET | Retrieves MTA-STS reports from DMARC Report. |

### Postmaster Account

| Action | Method | Description |
| --- | --- | --- |
| [List Connected Postmaster Accounts](actions/list-connected-postmaster-accounts.md) | GET | Retrieves connected postmaster accounts from DMARC Report. |

### Postmaster Account Record

| Action | Method | Description |
| --- | --- | --- |
| [Get Postmaster Account Record](actions/get-postmaster-account-record.md) | GET | Retrieves a postmaster account record from DMARC Report. |
| [List Postmaster Account Records](actions/list-postmaster-account-records.md) | GET | Retrieves postmaster account records from DMARC Report. |

