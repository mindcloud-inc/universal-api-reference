# <img src="https://images.mindcloud.co/apps/icons/datagma_1775059351993.png" alt="Datagma logo" width="28" height="28"> Datagma: Universal API

Datagma enriches B2B people and company data, finds verified work emails and phone numbers, detects job changes, and resolves Twitter identities from contact data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/datagma/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://datagma.com
- **Vendor API docs:** https://datagmaapi.readme.io/reference/getting-started-with-your-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credit](actions/get-credit.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datagma/latest/actions/get-credit?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Enrich a person or a company](actions/enrich-a-person-or-a-company.md) | GET | Retrieves person or company enrichment data from Datagma. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Find People](actions/find-people.md) | GET | Finds people in Datagma by company and job title. |
| [Search By Email (outside EU)](actions/search-by-email-outside-eu.md) | GET | Finds contacts in Datagma by email outside the EU. |
| [Search By Phone Numbers](actions/search-by-phone-numbers.md) | GET | Finds contacts in Datagma by phone number. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Find Work Verified Email](actions/find-work-verified-email.md) | GET | Finds a verified work email in Datagma. |

### Employments

| Action | Method | Description |
| --- | --- | --- |
| [Job Change Detection](actions/job-change-detection.md) | GET | Retrieves job change details from Datagma. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit](actions/get-credit.md) | GET | Retrieves account credit details from Datagma. |

### Phone Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Search Phone Numbers](actions/search-phone-numbers.md) | GET | Finds phone numbers in Datagma by email or profile. |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get Twitter By Email](actions/get-twitter-by-email.md) | GET | Retrieves Twitter profile data from Datagma by email. |
| [Get Twitter By Username](actions/get-twitter-by-username.md) | GET | Retrieves Twitter profile data from Datagma by username. |

