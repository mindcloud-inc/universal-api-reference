# Explorium: Native API Reference

A consolidated summary of Explorium's API configuration and 38 documented operations, with links to official documentation.

- **Official docs:** https://developers.explorium.ai/reference/businesses/businesses_api
- **API base URL:** `https://api.explorium.ai`

## Authentication

### API Key

Use your Explorium API key.

[Official authentication documentation](https://developers.explorium.ai/deprecated-docs/getting-your-api-key)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (38 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Businesses Enrollments](actions/add-businesses-enrollments.md) | `POST /v1/businesses/events/enrollments` | [docs](https://developers.explorium.ai/reference/businesses/events/add_businesses_enrollments) |
| [Add Prospects Enrollments](actions/add-prospects-enrollments.md) | `POST /v1/prospects/events/enrollments` | [docs](https://developers.explorium.ai/reference/prospects/events/add_prospects_enrollments) |
| [Add Webhook](actions/add-webhook.md) | `POST /v1/webhooks` | [docs](https://developers.explorium.ai/reference/webhooks/add_webhook) |
| [Autocomplete Businesses](actions/autocomplete-businesses.md) | `GET /v1/businesses/autocomplete` | [docs](https://developers.explorium.ai/reference/businesses/autocomplete/businesses_autocomplete) |
| [Autocomplete Prospects](actions/autocomplete-prospects.md) | `GET /v1/prospects/autocomplete` | [docs](https://developers.explorium.ai/reference/prospects/prospects_autocomplete) |
| [Check Webhook Connectivity](actions/check-webhook-connectivity.md) | `POST /v1/webhooks/check_connectivity` | [docs](https://developers.explorium.ai/reference/webhooks/check_webhook_connectivity) |
| [Delete Businesses Enrollments](actions/delete-businesses-enrollments.md) | `POST /v1/businesses/events/enrollments` | [docs](https://developers.explorium.ai/reference/businesses/events/delete_businesses_enrollments) |
| [Delete Prospects Enrollments](actions/delete-prospects-enrollments.md) | `POST /v1/prospects/events/enrollments` | [docs](https://developers.explorium.ai/reference/prospects/events/delete_prospects_enrollments) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /v1/webhooks/{{partner_id}}` | [docs](https://developers.explorium.ai/reference/webhooks/delete_webhook) |
| [Enrich Company Ratings](actions/enrich-company-ratings.md) | `POST /v1/businesses/company_ratings_by_employees/enrich` | [docs](https://developers.explorium.ai/reference/businesses/enrichments/company_ratings) |
| [Enrich Company Social Media](actions/enrich-company-social-media.md) | `POST /v1/businesses/linkedin_posts/enrich` | [docs](https://developers.explorium.ai/reference/businesses/enrichments/company_social_media) |
| [Enrich Contact Details](actions/enrich-contact-details.md) | `POST /v1/prospects/contacts_information/enrich` | [docs](https://developers.explorium.ai/reference/prospects/enrichments/contacts_information) |
| [Enrich Financial Metrics](actions/enrich-financial-metrics.md) | `POST /v1/businesses/financial_indicators/enrich` | [docs](https://developers.explorium.ai/reference/businesses/enrichments/financial_metrics_for_public_companies) |
| [Enrich Firmographics](actions/enrich-firmographics.md) | `POST /v1/businesses/firmographics/enrich` | [docs](https://developers.explorium.ai/reference/businesses/enrichments/firmographics) |
| [Enrich Funding and Acquisitions](actions/enrich-funding-and-acquisitions.md) | `POST /v1/businesses/funding_and_acquisition/enrich` | [docs](https://developers.explorium.ai/reference/businesses/enrichments/funding_and_acquisitions) |
| [Enrich Lookalike Companies](actions/enrich-lookalike-companies.md) | `POST /v1/businesses/lookalikes/enrich` | [docs](https://developers.explorium.ai/reference/businesses/enrichments/lookalike-companies) |
| [Enrich Professional Profile](actions/enrich-professional-profile.md) | `POST /v1/prospects/profiles/enrich` | [docs](https://developers.explorium.ai/reference/prospects/enrichments/professional_profile_contact_and_workplace) |
| [Enrich Prospect Social Media](actions/enrich-prospect-social-media.md) | `POST /v1/prospects/linkedin_posts/enrich` | [docs](https://developers.explorium.ai/reference/prospects/enrichments/individual_social_media_presence) |
| [Enrich Technographics](actions/enrich-technographics.md) | `POST /v1/businesses/technographics/enrich` | [docs](https://developers.explorium.ai/reference/businesses/enrichments/technographics) |
| [Enrich Website Content Changes](actions/enrich-website-content-changes.md) | `POST /v1/businesses/website_changes/enrich` | [docs](https://developers.explorium.ai/reference/businesses/enrichments/company_website_content_changes) |
| [Enrich Website Keywords](actions/enrich-website-keywords.md) | `POST /v1/businesses/company_website_keywords/enrich` | [docs](https://developers.explorium.ai/reference/businesses/enrichments/keyword_search_on_websites) |
| [Enrich Webstack](actions/enrich-webstack.md) | `POST /v1/businesses/webstack/enrich` | [docs](https://developers.explorium.ai/reference/businesses/enrichments/webstack) |
| [Enrich Workforce Trends](actions/enrich-workforce-trends.md) | `POST /v1/businesses/workforce_trends/enrich` | [docs](https://developers.explorium.ai/reference/businesses/enrichments/workforce_trends) |
| [Fetch Businesses](actions/fetch-businesses.md) | `POST /v1/businesses` | [docs](https://developers.explorium.ai/reference/businesses/fetch_businesses) |
| [Fetch Businesses Events](actions/fetch-businesses-events.md) | `POST /v1/businesses/events` | [docs](https://developers.explorium.ai/reference/businesses/events/fetch_businesses_events) |
| [Fetch Prospects](actions/fetch-prospects.md) | `POST /v1/prospects` | [docs](https://developers.explorium.ai/reference/prospects/fetch_prospects) |
| [Fetch Prospects Events](actions/fetch-prospects-events.md) | `POST /v1/prospects/events` | [docs](https://developers.explorium.ai/reference/prospects/events/fetch_prospects_events) |
| [Get Active Credits Summary](actions/get-active-credits-summary.md) | `GET /v1/credits` | [docs](https://developers.explorium.ai/reference/credits/get_active_credits_summary) |
| [Get Business Statistics](actions/get-business-statistics.md) | `POST /v1/businesses/stats` | [docs](https://developers.explorium.ai/reference/businesses/fetch_businesses_statistics) |
| [Get Businesses Enrollments](actions/get-businesses-enrollments.md) | `POST /v1/businesses/events/enrollments` | [docs](https://developers.explorium.ai/reference/businesses/events/get_businesses_enrollments) |
| [Get Credit Consumption Aggregation](actions/get-credit-consumption-aggregation.md) | `POST /v1/credits/aggregation` | [docs](https://developers.explorium.ai/reference/credits/get_credit_consumption_aggregation) |
| [Get Prospects Enrollments](actions/get-prospects-enrollments.md) | `POST /v1/prospects/events/enrollments` | [docs](https://developers.explorium.ai/reference/prospects/events/get_prospects_enrollments) |
| [Get Prospects Statistics](actions/get-prospects-statistics.md) | `POST /v1/prospects/stats` | [docs](https://developers.explorium.ai/reference/prospects/prospects_stats) |
| [Get Webhook](actions/get-webhook.md) | `GET /v1/webhooks/{{partner_id}}` | [docs](https://developers.explorium.ai/reference/webhooks/get_webhook) |
| [Match Businesses](actions/match-businesses.md) | `POST /v1/businesses/match` | [docs](https://developers.explorium.ai/reference/businesses/match_businesses) |
| [Match Prospects](actions/match-prospects.md) | `POST /v1/prospects/match` | [docs](https://developers.explorium.ai/reference/prospects/match_prospects) |
| [Update Businesses Enrollments](actions/update-businesses-enrollments.md) | `POST /v1/businesses/events/enrollments` | [docs](https://developers.explorium.ai/reference/businesses/events/update_businesses_enrollments) |
| [Update Prospects Enrollments](actions/update-prospects-enrollments.md) | `POST /v1/prospects/events/enrollments` | [docs](https://developers.explorium.ai/reference/prospects/events/update_prospects_enrollments) |
