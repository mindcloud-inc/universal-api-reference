# <img src="https://images.mindcloud.co/apps/icons/id1brds-tlf-1774385072022_1774385077609.png" alt="UpGuard logo" width="28" height="28"> UpGuard: Universal API

Monitor cyber risk across vendors, assets, and workforce

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/upGuard/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.upguard.com
- **Vendor API docs:** https://cyber-risk.upguard.com/api/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Available Risks](actions/list-available-risks.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/upGuard/latest/actions/list-available-risks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Available Risk

| Action | Method | Description |
| --- | --- | --- |
| [List Available Risks](actions/list-available-risks.md) | GET | Retrieves available risk definitions from the UpGuard platform. |

### Breached Identity

| Action | Method | Description |
| --- | --- | --- |
| [List Breached Identities](actions/list-breached-identities.md) | GET | Retrieves breached identities from your UpGuard account. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from your UpGuard account. |
| [Retrieve Domain Details](actions/retrieve-domain-details.md) | GET | Retrieves details for a domain in UpGuard. |
| [Update Domain Labels](actions/update-domain-labels.md) | PUT | Updates labels for a domain in UpGuard. |

### Identity Breach

| Action | Method | Description |
| --- | --- | --- |
| [Get Identity Breach Details](actions/get-identity-breach-details.md) | GET | Retrieves details for an identity breach in UpGuard. |

### Ip

| Action | Method | Description |
| --- | --- | --- |
| [List IPs](actions/list-ips.md) | GET | Retrieves IP addresses from your UpGuard account. |
| [Retrieve IP Details](actions/retrieve-ip-details.md) | GET | Retrieves details for an IP address in UpGuard. |
| [Update IP Labels](actions/update-ip-labels.md) | PUT | Updates labels for an IP address in UpGuard. |

### Ip Range

| Action | Method | Description |
| --- | --- | --- |
| [List IP Ranges](actions/list-ip-ranges.md) | GET | Retrieves IP ranges from your UpGuard account. |

### Label

| Action | Method | Description |
| --- | --- | --- |
| [List Labels](actions/list-labels.md) | GET | Retrieves registered labels from your UpGuard account. |

### Onboarding Request

| Action | Method | Description |
| --- | --- | --- |
| [Get Onboarding Request](actions/get-onboarding-request.md) | GET | Retrieves an onboarding request from UpGuard. |
| [List Onboarding Requests](actions/list-onboarding-requests.md) | GET | Retrieves onboarding requests from your UpGuard account. |

### Organisation

| Action | Method | Description |
| --- | --- | --- |
| [Get Organisation](actions/get-organisation.md) | GET | Retrieves your organisation details from UpGuard. |

### Risk

| Action | Method | Description |
| --- | --- | --- |
| [Get Risk Details](actions/get-risk-details.md) | GET | Retrieves details for an UpGuard risk. |
| [List Active Risks](actions/list-active-risks.md) | GET | Retrieves active risks for your UpGuard account. |

### Risk Diff

| Action | Method | Description |
| --- | --- | --- |
| [List Risk Changes](actions/list-risk-changes.md) | GET | Retrieves risk changes for your UpGuard account. |

### Typosquat Domain

| Action | Method | Description |
| --- | --- | --- |
| [List Typosquat Domains](actions/list-typosquat-domains.md) | GET | Retrieves typosquat domains from your UpGuard account. |
| [Retrieve Typosquat Details](actions/retrieve-typosquat-details.md) | GET | Retrieves typosquat details for a domain in UpGuard. |

### Vendor

| Action | Method | Description |
| --- | --- | --- |
| [Get Vendor Details](actions/get-vendor-details.md) | GET | Retrieves details for a vendor in UpGuard. |
| [List Monitored Vendors](actions/list-monitored-vendors.md) | GET | Retrieves monitored vendors from your UpGuard portfolio. |
| [Start Monitoring Vendor](actions/start-monitoring-vendor.md) | POST | Starts monitoring a vendor in UpGuard. |
| [Stop Monitoring Vendor](actions/stop-monitoring-vendor.md) | DELETE | Stops monitoring a vendor in UpGuard. |
| [Update Vendor Attributes](actions/update-vendor-attributes.md) | PUT | Updates attributes for a vendor in UpGuard. |
| [Update Vendor Labels](actions/update-vendor-labels.md) | PUT | Updates labels for a vendor in UpGuard. |
| [Update Vendor Tier](actions/update-vendor-tier.md) | PUT | Updates the tier for a vendor in UpGuard. |

### Vendor Domain

| Action | Method | Description |
| --- | --- | --- |
| [List Vendor Domains](actions/list-vendor-domains.md) | GET | Retrieves domains for a monitored vendor in UpGuard. |
| [Retrieve Vendor Domain Details](actions/retrieve-vendor-domain-details.md) | GET | Retrieves details for a vendor domain in UpGuard. |

### Vendor Ip

| Action | Method | Description |
| --- | --- | --- |
| [List Vendor IPs](actions/list-vendor-ips.md) | GET | Retrieves IP addresses for a vendor in UpGuard. |
| [Retrieve Vendor IP Details](actions/retrieve-vendor-ip-details.md) | GET | Retrieves details for a vendor IP address in UpGuard. |

### Vendor Questionnaire

| Action | Method | Description |
| --- | --- | --- |
| [Get Vendor Questionnaire Metadata](actions/get-vendor-questionnaire-metadata.md) | GET | Retrieves metadata for a vendor questionnaire in UpGuard. |
| [List Vendor Questionnaires](actions/list-vendor-questionnaires.md) | GET | Retrieves vendor questionnaires from your UpGuard account. |
| [Send Security Questionnaire To Vendor](actions/send-security-questionnaire-to-vendor.md) | POST | Sends a security questionnaire to a vendor in UpGuard. |

### Vendor Questionnaire Answer

| Action | Method | Description |
| --- | --- | --- |
| [Get Vendor Questionnaire Questions And Answers](actions/get-vendor-questionnaire-questions-and-answers.md) | GET | Retrieves questionnaire questions and answers from UpGuard. |

### Vendor Risk

| Action | Method | Description |
| --- | --- | --- |
| [List Vendor Risks](actions/list-vendor-risks.md) | GET | Retrieves active risks for a vendor in UpGuard. |

### Vendor Risk Diff

| Action | Method | Description |
| --- | --- | --- |
| [List Monitored Vendor Risk Changes](actions/list-monitored-vendor-risk-changes.md) | GET | Retrieves risk changes for monitored vendors in UpGuard. |

### Vendor Risk Overview

| Action | Method | Description |
| --- | --- | --- |
| [Get Portfolio Risk Profile Overview](actions/get-portfolio-risk-profile-overview.md) | GET | Retrieves a portfolio risk overview from UpGuard. |

### Vendor Vulnerability

| Action | Method | Description |
| --- | --- | --- |
| [List Vendor Vulnerabilities](actions/list-vendor-vulnerabilities.md) | GET | Retrieves potential vulnerabilities for a vendor in UpGuard. |

### Vendor With Risk

| Action | Method | Description |
| --- | --- | --- |
| [List Vendors Affected By Risk](actions/list-vendors-affected-by-risk.md) | GET | Retrieves vendors affected by a risk in UpGuard. |

### Vulnerability

| Action | Method | Description |
| --- | --- | --- |
| [List Vulnerabilities](actions/list-vulnerabilities.md) | GET | Retrieves potential vulnerabilities from your UpGuard account. |

