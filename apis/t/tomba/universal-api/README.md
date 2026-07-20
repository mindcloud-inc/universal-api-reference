# <img src="https://images.mindcloud.co/apps/icons/tomba_1774362579643.png" alt="Tomba logo" width="28" height="28"> Tomba: Universal API

Find, verify, and enrich professional contact and company data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tomba/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tomba.io
- **Vendor API docs:** https://docs.tomba.io/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tomba/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves the current account from Tomba. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Find Company](actions/find-company.md) | GET | Retrieves company enrichment data from Tomba. |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in Tomba by search filters. |
| [Similar Domains](actions/similar-domains.md) | GET | Finds similar domains in Tomba. |
| [Technology](actions/technology.md) | GET | Retrieves company technology data from Tomba. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Domain Status](actions/domain-status.md) | GET | Retrieves the status of a domain in Tomba. |
| [Email Count](actions/email-count.md) | GET | Retrieves the email count for a company in Tomba. |
| [Email Format](actions/email-format.md) | GET | Retrieves email format details for a company in Tomba. |
| [Get Domain Suggestions](actions/get-domain-suggestions.md) | GET | Finds domain suggestions in Tomba. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Author Finder](actions/author-finder.md) | GET | Finds author contact details in Tomba. |
| [Domain Search](actions/domain-search.md) | GET | Finds contacts in Tomba by domain. |
| [Email Enrichment](actions/email-enrichment.md) | GET | Retrieves contact enrichment data from Tomba. |
| [Email Finder](actions/email-finder.md) | GET | Finds a contact email in Tomba. |
| [Email Sources](actions/email-sources.md) | GET | Retrieves email sources from Tomba. |
| [Email Verifier](actions/email-verifier.md) | GET | Verifies an email address in Tomba. |
| [LinkedIn Finder](actions/linked-in-finder.md) | GET | Finds contact details from LinkedIn in Tomba. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Combined Enrichment](actions/combined-enrichment.md) | GET | Retrieves combined enrichment data from Tomba. |
| [Find Person](actions/find-person.md) | GET | Retrieves person enrichment data from Tomba. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from Tomba. |

### Lead List

| Action | Method | Description |
| --- | --- | --- |
| [List Lead Lists](actions/list-lead-lists.md) | GET | Retrieves lead lists from Tomba. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Location](actions/location.md) | GET | Retrieves location data from Tomba. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [Phone Finder](actions/phone-finder.md) | GET | Finds a phone number in Tomba. |
| [Phone Validator](actions/phone-validator.md) | GET | Validates a phone number in Tomba. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve API Usage](actions/retrieve-api-usage.md) | GET | Retrieves API usage details from Tomba. |

