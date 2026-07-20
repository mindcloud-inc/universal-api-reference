# <img src="https://images.mindcloud.co/apps/icons/explorium-icon_1775829739479.png" alt="Explorium logo" width="28" height="28"> Explorium: Universal API

Enrich businesses and prospects with data, signals, and events

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/exploriumAPI/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.explorium.ai
- **Vendor API docs:** https://developers.explorium.ai/reference/businesses/businesses_api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Active Credits Summary](actions/get-active-credits-summary.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exploriumAPI/latest/actions/get-active-credits-summary?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Business

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Businesses](actions/fetch-businesses.md) | GET | Fetches businesses from Explorium API. |
| [Match Businesses](actions/match-businesses.md) | GET | Matches businesses in Explorium API. |

### Business Autocomplete

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Businesses](actions/autocomplete-businesses.md) | GET | Retrieves business autocomplete results from Explorium API. |

### Business Enrollment

| Action | Method | Description |
| --- | --- | --- |
| [Add Businesses Enrollments](actions/add-businesses-enrollments.md) | POST | Adds business event enrollments in Explorium API. |
| [Delete Businesses Enrollments](actions/delete-businesses-enrollments.md) | DELETE | Deletes business event enrollments from Explorium API. |
| [Get Businesses Enrollments](actions/get-businesses-enrollments.md) | GET | Retrieves business event enrollments from Explorium API. |
| [Update Businesses Enrollments](actions/update-businesses-enrollments.md) | PUT | Updates business event enrollments in Explorium API. |

### Business Event

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Businesses Events](actions/fetch-businesses-events.md) | GET | Fetches business events from Explorium API. |

### Business Firmographics

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Firmographics](actions/enrich-firmographics.md) | GET | Enriches businesses with firmographics in Explorium API. |

### Business Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Business Statistics](actions/get-business-statistics.md) | GET | Retrieves business statistics from Explorium API. |

### Business Technographics

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Technographics](actions/enrich-technographics.md) | GET | Enriches businesses with technographics in Explorium API. |

### Company Ratings

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Company Ratings](actions/enrich-company-ratings.md) | GET | Enriches businesses with company ratings in Explorium API. |

### Company Social Media

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Company Social Media](actions/enrich-company-social-media.md) | GET | Enriches businesses with company social media in Explorium API. |

### Contact Details

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Contact Details](actions/enrich-contact-details.md) | GET | Enriches prospects with contact details in Explorium API. |

### Credit Consumption

| Action | Method | Description |
| --- | --- | --- |
| [Get Credit Consumption Aggregation](actions/get-credit-consumption-aggregation.md) | GET | Retrieves credit consumption aggregation from Explorium API. |

### Credit Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Active Credits Summary](actions/get-active-credits-summary.md) | GET | Retrieves active credits summary from Explorium API. |

### Financial Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Financial Metrics](actions/enrich-financial-metrics.md) | GET | Enriches businesses with financial metrics in Explorium API. |

### Funding And Acquisitions

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Funding and Acquisitions](actions/enrich-funding-and-acquisitions.md) | GET | Enriches businesses with funding and acquisitions in Explorium API. |

### Lookalike Companies

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Lookalike Companies](actions/enrich-lookalike-companies.md) | GET | Enriches businesses with lookalike companies in Explorium API. |

### Professional Profile

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Professional Profile](actions/enrich-professional-profile.md) | GET | Enriches prospects with professional profile data in Explorium API. |

### Prospect

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Prospects](actions/fetch-prospects.md) | GET | Fetches prospects from Explorium API. |
| [Match Prospects](actions/match-prospects.md) | GET | Matches prospects in Explorium API. |

### Prospect Autocomplete

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Prospects](actions/autocomplete-prospects.md) | GET | Retrieves prospect autocomplete results from Explorium API. |

### Prospect Enrollment

| Action | Method | Description |
| --- | --- | --- |
| [Add Prospects Enrollments](actions/add-prospects-enrollments.md) | POST | Adds prospect event enrollments in Explorium API. |
| [Delete Prospects Enrollments](actions/delete-prospects-enrollments.md) | DELETE | Deletes prospect event enrollments from Explorium API. |
| [Get Prospects Enrollments](actions/get-prospects-enrollments.md) | GET | Retrieves prospect event enrollments from Explorium API. |
| [Update Prospects Enrollments](actions/update-prospects-enrollments.md) | PUT | Updates prospect event enrollments in Explorium API. |

### Prospect Event

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Prospects Events](actions/fetch-prospects-events.md) | GET | Fetches prospect events from Explorium API. |

### Prospect Social Media

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Prospect Social Media](actions/enrich-prospect-social-media.md) | GET | Enriches prospects with social media in Explorium API. |

### Prospect Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Prospects Statistics](actions/get-prospects-statistics.md) | GET | Retrieves prospect statistics from Explorium API. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Add Webhook](actions/add-webhook.md) | POST | Creates a webhook in Explorium API. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Explorium API. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Explorium API. |

### Webhook Connectivity

| Action | Method | Description |
| --- | --- | --- |
| [Check Webhook Connectivity](actions/check-webhook-connectivity.md) | GET | Checks webhook connectivity in Explorium API. |

### Website Content Changes

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Website Content Changes](actions/enrich-website-content-changes.md) | GET | Enriches businesses with website content changes in Explorium API. |

### Website Keywords

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Website Keywords](actions/enrich-website-keywords.md) | GET | Enriches businesses with website keywords in Explorium API. |

### Webstack

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Webstack](actions/enrich-webstack.md) | GET | Enriches businesses with webstack data in Explorium API. |

### Workforce Trends

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Workforce Trends](actions/enrich-workforce-trends.md) | GET | Enriches businesses with workforce trends in Explorium API. |

