# <img src="https://images.mindcloud.co/apps/icons/piloterr-icon_1775072024314.png" alt="Piloterr logo" width="28" height="28"> Piloterr: Universal API

Piloterr provides API endpoints for search, company intelligence, website analysis, marketplace data extraction, and profile enrichment across public web sources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/piloterr/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://piloterr.com
- **Vendor API docs:** https://docs.piloterr.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage](actions/get-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piloterr/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Crunchbase Company Info](actions/get-crunchbase-company-info.md) | GET |  |
| [Get LinkedIn Company Info](actions/get-linkedin-company-info.md) | GET |  |
| [Get Owler Company Info](actions/get-owler-company-info.md) | GET |  |
| [Get Trustpilot Company Info](actions/get-trustpilot-company-info.md) | GET |  |
| [Search Crunchbase](actions/search-crunchbase.md) | GET |  |
| [Search Owler Companies](actions/search-owler-companies.md) | GET |  |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Get LinkedIn Job Info](actions/get-linkedin-job-info.md) | GET |  |
| [Search Google Jobs](actions/search-google-jobs.md) | GET |  |
| [Search LinkedIn Jobs](actions/search-linkedin-jobs.md) | GET |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get LinkedIn Product Info](actions/get-linkedin-product-info.md) | GET |  |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Email Domain](actions/analyze-email-domain.md) | GET |  |
| [Check Domain DNSBL](actions/check-domain-dnsbl.md) | GET |  |
| [Check Domain Malicious](actions/check-domain-malicious.md) | GET |  |
| [Count LinkedIn Jobs](actions/count-linkedin-jobs.md) | GET |  |
| [Detect Website Technologies](actions/detect-website-technologies.md) | GET |  |
| [Find Professional Email](actions/find-professional-email.md) | GET |  |
| [Get Crunchbase Funding Round](actions/get-crunchbase-funding-round.md) | GET |  |
| [Get Google Search Autocomplete](actions/get-google-search-autocomplete.md) | GET |  |
| [Get LinkedIn Post Info](actions/get-linkedin-post-info.md) | GET |  |
| [Get Similarweb Domain](actions/get-similarweb-domain.md) | GET |  |
| [Get Usage](actions/get-usage.md) | GET |  |
| [List Crunchbase Funding Rounds](actions/list-crunchbase-funding-rounds.md) | GET |  |
| [Lookup Domain Whois](actions/lookup-domain-whois.md) | GET |  |
| [Search Bing](actions/search-bing.md) | GET |  |
| [Search Brave](actions/search-brave.md) | GET |  |
| [Search Google](actions/search-google.md) | GET |  |
| [Search Google Images](actions/search-google-images.md) | GET |  |
| [Search Google News](actions/search-google-news.md) | GET |  |
| [Search Google Videos](actions/search-google-videos.md) | GET |  |
| [Search Similarweb](actions/search-similarweb.md) | GET |  |
| [Verify Email Address](actions/verify-email-address.md) | GET |  |

### User Profiles

| Action | Method | Description |
| --- | --- | --- |
| [Get Crunchbase People Info](actions/get-crunchbase-people-info.md) | GET |  |
| [Get LinkedIn Profile Info](actions/get-linkedin-profile-info.md) | GET |  |

