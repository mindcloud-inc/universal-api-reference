# <img src="https://images.mindcloud.co/apps/icons/nyne-ai_1776859837917.png" alt="Nyne AI logo" width="28" height="28"> Nyne AI: Universal API

Nyne AI provides APIs for person enrichment, people search, social intelligence, company enrichment, company discovery, funding, and seller/feature checks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nyneAI/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nyne.ai/
- **Vendor API docs:** https://api.nyne.ai/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get API Usage](actions/get-api-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/get-api-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Article

| Action | Method | Description |
| --- | --- | --- |
| [Search Person Articles](actions/search-person-articles.md) | GET | Retrieves articles about a person from Nyne AI. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Discover Companies From Web](actions/discover-companies-from-web.md) | GET | Finds companies from web research in Nyne AI. |
| [Enrich Company](actions/enrich-company.md) | GET | Retrieves enriched details for a company from Nyne AI. |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in Nyne AI by industry or keyword. |

### Company Need

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Company Needs](actions/analyze-company-needs.md) | GET | Retrieves company pain points from Nyne AI. |

### Competitor Engagement

| Action | Method | Description |
| --- | --- | --- |
| [Get Competitor Engagements](actions/get-competitor-engagements.md) | GET | Retrieves competitor engagements for people from Nyne AI. |

### Feature Check

| Action | Method | Description |
| --- | --- | --- |
| [Check Company Feature](actions/check-company-feature.md) | GET | Retrieves feature detection details for a company from Nyne AI. |

### Funding

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Funding](actions/get-company-funding.md) | GET | Retrieves company funding details from Nyne AI. |

### Investor

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Investor](actions/lookup-investor.md) | GET | Retrieves investor fund profiles from Nyne AI. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Find Person Leads](actions/find-person-leads.md) | GET | Finds person leads in Nyne AI. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Discover People By Keywords](actions/discover-people-by-keywords.md) | GET | Finds people in Nyne AI by keywords. |
| [Discover People From Web](actions/discover-people-from-web.md) | GET | Finds people from web research in Nyne AI. |
| [Enrich Person](actions/enrich-person.md) | GET | Retrieves enriched details for a person from Nyne AI. |
| [Find Event Attendees](actions/find-event-attendees.md) | GET | Finds people attending an event in Nyne AI. |
| [Search People](actions/search-people.md) | GET | Finds people in Nyne AI by natural-language query. |

### Person Answer

| Action | Method | Description |
| --- | --- | --- |
| [Ask About Person](actions/ask-about-person.md) | GET | Retrieves answers about a person from Nyne AI. |

### Person Research

| Action | Method | Description |
| --- | --- | --- |
| [Deep Research Person](actions/deep-research-person.md) | GET | Retrieves deep research about a person from Nyne AI. |

### Person Simulation

| Action | Method | Description |
| --- | --- | --- |
| [Simulate Person Response](actions/simulate-person-response.md) | GET | Retrieves a simulated response from a person in Nyne AI. |

### Personal Interest

| Action | Method | Description |
| --- | --- | --- |
| [Discover Personal Interests](actions/discover-personal-interests.md) | GET | Retrieves personal interests for a person from Nyne AI. |

### Seller Check

| Action | Method | Description |
| --- | --- | --- |
| [Check Company Seller Fit](actions/check-company-seller-fit.md) | GET | Retrieves seller fit details for a company from Nyne AI. |

### Social Interaction

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Social Interactions](actions/fetch-social-interactions.md) | GET | Retrieves social interactions for a person from Nyne AI. |

### Social Post

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Person Newsfeed](actions/fetch-person-newsfeed.md) | GET | Retrieves social media posts for a person from Nyne AI. |

### Social Profile

| Action | Method | Description |
| --- | --- | --- |
| [Find Single Social Profile](actions/find-single-social-profile.md) | GET | Retrieves one social profile for a person from Nyne AI. |
| [Find Social Profiles](actions/find-social-profiles.md) | GET | Retrieves social profiles for a person from Nyne AI. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get API Usage](actions/get-api-usage.md) | GET | Retrieves API usage details from Nyne AI. |

