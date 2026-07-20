# Nyne AI: Native API Reference

A consolidated summary of Nyne AI's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://api.nyne.ai/documentation
- **OpenAPI specification:** https://api.nyne.ai/.well-known/nyne-api.json
- **API base URL:** `https://api.nyne.ai`

## Authentication

### API Key and Secret

Authenticate Nyne API requests with X-API-Key and X-API-Secret headers.

### Credentials

- **API Key:** `apiKey` · required
- **API Secret:** `apiSecret` · required · Nyne API secret sent in the X-API-Secret header.

Send these headers with each API request:

```http
X-API-Key: <apiKey>
X-API-Secret: <apiSecret>
```

[Official authentication documentation](https://api.nyne.ai/documentation/person/enrichment)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Analyze Company Needs](actions/analyze-company-needs.md) | `POST /company/needs` | [docs](https://api.nyne.ai/documentation/company/needs) |
| [Ask About Person](actions/ask-about-person.md) | `POST /person/ask` | [docs](https://api.nyne.ai/documentation/person/ask) |
| [Check Company Feature](actions/check-company-feature.md) | `POST /company/checkfeature` | [docs](https://api.nyne.ai/documentation/company/checkfeature) |
| [Check Company Seller Fit](actions/check-company-seller-fit.md) | `POST /company/checkseller` | [docs](https://api.nyne.ai/documentation/company/checkseller) |
| [Deep Research Person](actions/deep-research-person.md) | `POST /person/deep-research` | [docs](https://api.nyne.ai/documentation/person/deep-research) |
| [Discover Companies From Web](actions/discover-companies-from-web.md) | `POST /company/discovery` | [docs](https://api.nyne.ai/documentation/company/discovery) |
| [Discover People By Keywords](actions/discover-people-by-keywords.md) | `POST /person/discover` | [docs](https://api.nyne.ai/documentation/person/discover) |
| [Discover People From Web](actions/discover-people-from-web.md) | `POST /person/discovery` | [docs](https://api.nyne.ai/documentation/person/discovery) |
| [Discover Personal Interests](actions/discover-personal-interests.md) | `POST /person/interests` | [docs](https://api.nyne.ai/documentation/person/interests) |
| [Enrich Company](actions/enrich-company.md) | `POST /company/enrichment` | [docs](https://api.nyne.ai/documentation/company/enrichment) |
| [Enrich Person](actions/enrich-person.md) | `POST /person/enrichment` | [docs](https://api.nyne.ai/documentation/person/enrichment) |
| [Fetch Person Newsfeed](actions/fetch-person-newsfeed.md) | `POST /person/newsfeed` | [docs](https://api.nyne.ai/documentation/person/newsfeed) |
| [Fetch Social Interactions](actions/fetch-social-interactions.md) | `POST /person/interactions` | [docs](https://api.nyne.ai/documentation/person/interactions) |
| [Find Event Attendees](actions/find-event-attendees.md) | `POST /person/events` | [docs](https://api.nyne.ai/documentation/person/events) |
| [Find Person Leads](actions/find-person-leads.md) | `POST /person/leads` | [docs](https://api.nyne.ai/documentation/person/leads) |
| [Find Single Social Profile](actions/find-single-social-profile.md) | `POST /person/single-social-lookup` | [docs](https://api.nyne.ai/documentation/person/single-social-lookup) |
| [Find Social Profiles](actions/find-social-profiles.md) | `POST /person/social-profiles` | [docs](https://api.nyne.ai/documentation/person/social-profiles) |
| [Get API Usage](actions/get-api-usage.md) | `GET /usage` | [docs](https://api.nyne.ai/documentation/usage) |
| [Get Company Funding](actions/get-company-funding.md) | `POST /company/funding` | [docs](https://api.nyne.ai/documentation/company/funding) |
| [Get Competitor Engagements](actions/get-competitor-engagements.md) | `POST /person/competitor-engagements` | [docs](https://api.nyne.ai/documentation/person/competitor-engagements) |
| [Lookup Investor](actions/lookup-investor.md) | `POST /company/funders` | [docs](https://api.nyne.ai/documentation/company/funders) |
| [Search Companies](actions/search-companies.md) | `POST /company/search` | [docs](https://api.nyne.ai/documentation/company/search) |
| [Search People](actions/search-people.md) | `POST /person/search` | [docs](https://api.nyne.ai/documentation/person/search) |
| [Search Person Articles](actions/search-person-articles.md) | `POST /person/articlesearch` | [docs](https://api.nyne.ai/documentation/person/articlesearch) |
| [Simulate Person Response](actions/simulate-person-response.md) | `POST /person/simulation` | [docs](https://api.nyne.ai/documentation/person/simulation) |
