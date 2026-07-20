# Influencers.club: Native API Reference

A consolidated summary of Influencers.club's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://docs.influencers.club
- **API base URL:** `https://api-dashboard.influencers.club`

## Authentication

### API Key

Use your Influencers.club API key from dashboard.influencers.club.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.influencers.club/)

## Pagination

Use `paging.limit` in the request body to set the page size (default 5; accepted range 1–50). Use `paging.page` in the request body to choose the page; numbering starts at 0.

## Filtering

Send filters in the request body.

## Sorting

Set the sort field with `sort.sort_by` in the request body. Set the direction separately with `sort.sort_order`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,503`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Compare Creator Audience Overlap](actions/compare-creator-audience-overlap.md) | `POST /public/v1/creators/audience/overlap/` | [docs](https://docs.influencers.club/openapi/audience-overlap/public_v1_creators_audience_overlap_create) |
| [Create Enrichment Batch](actions/create-enrichment-batch.md) | `POST /public/v1/enrichment/batch/` | [docs](https://docs.influencers.club/openapi/batch-enrichment/public_v1_enrichment_batch_create) |
| [Enrich Creator By Email](actions/enrich-creator-by-email.md) | `POST /public/v1/creators/enrich/email/` | [docs](https://docs.influencers.club/openapi/enrich-by-email/public_v1_creators_enrich_email_create) |
| [Enrich Creator By Handle (Full)](actions/enrich-creator-by-handle-full.md) | `POST /public/v1/creators/enrich/handle/full/` | [docs](https://docs.influencers.club/openapi/enrich-by-handle-full/public_v1_creators_enrich_handle_full_create) |
| [Enrich Creator By Handle (Raw)](actions/enrich-creator-by-handle-raw.md) | `POST /public/v1/creators/enrich/handle/raw/` | [docs](https://docs.influencers.club/openapi/enrich-by-handle-raw/public_v1_creators_enrich_handle_raw_create) |
| [Find Creator Connected Socials](actions/find-creator-connected-socials.md) | `POST /public/v1/creators/socials/` | [docs](https://docs.influencers.club/openapi/connected-socials/public_v1_creators_socials_create) |
| [Find Similar Creators](actions/find-similar-creators.md) | `POST /public/v1/discovery/creators/similar/` | [docs](https://docs.influencers.club/openapi/similar-creators/public_v1_discovery_creators_similar_create) |
| [Get Creator Content Details](actions/get-creator-content-details.md) | `POST /public/v1/creators/content/details/` | [docs](https://docs.influencers.club/openapi/post-details/public_v1_creators_content_details_create) |
| [List Audience Brand Categories](actions/list-audience-brand-categories.md) | `GET /public/v1/discovery/classifier/audience-brand-categories/` | [docs](https://docs.influencers.club/openapi/dictionary/public_v1_discovery_classifier_audience_brand_categories_list) |
| [List Audience Brand Names](actions/list-audience-brand-names.md) | `GET /public/v1/discovery/classifier/audience-brand-names/` | [docs](https://docs.influencers.club/openapi/dictionary/public_v1_discovery_classifier_audience_brand_names_list) |
| [List Audience Interests](actions/list-audience-interests.md) | `GET /public/v1/discovery/classifier/audience-interests/` | [docs](https://docs.influencers.club/openapi/dictionary/public_v1_discovery_classifier_audience_interests_list) |
| [List Audience Locations](actions/list-audience-locations.md) | `GET /public/v1/discovery/classifier/audience-locations/` | [docs](https://docs.influencers.club/openapi/dictionary/public_v1_discovery_classifier_audience_locations_list) |
| [List Creator Content Posts](actions/list-creator-content-posts.md) | `POST /public/v1/creators/content/posts/` | [docs](https://docs.influencers.club/openapi/creator-posts/public_v1_creators_content_posts_create) |
| [List Discovery Brands](actions/list-discovery-brands.md) | `GET /public/v1/discovery/classifier/brands/` | [docs](https://docs.influencers.club/openapi/dictionary/public_v1_discovery_classifier_brands_list) |
| [List Discovery Games](actions/list-discovery-games.md) | `GET /public/v1/discovery/classifier/games/` | [docs](https://docs.influencers.club/openapi/dictionary/public_v1_discovery_classifier_games_list) |
| [List Discovery Languages](actions/list-discovery-languages.md) | `GET /public/v1/discovery/classifier/languages/` | [docs](https://docs.influencers.club/openapi/dictionary/public_v1_discovery_classifier_languages_list) |
| [List Discovery Locations By Platform](actions/list-discovery-locations-by-platform.md) | `GET /public/v1/discovery/classifier/locations/:platform/` | [docs](https://docs.influencers.club/openapi/dictionary/public_v1_discovery_classifier_locations_retrieve) |
| [List Discovery YouTube Topics](actions/list-discovery-youtube-topics.md) | `GET /public/v1/discovery/classifier/yt-topics/` | [docs](https://docs.influencers.club/openapi/dictionary/public_v1_discovery_classifier_yt_topics_list) |
| [Resume Enrichment Batch](actions/resume-enrichment-batch.md) | `POST /public/v1/enrichment/batch/:batch_id/resume/` | [docs](https://docs.influencers.club/openapi/batch-enrichment/public_v1_enrichment_batch_resume_create) |
| [Retrieve Account Credits And Usage](actions/retrieve-account-credits-and-usage.md) | `GET /public/v1/accounts/credits/` | [docs](https://docs.influencers.club/openapi/account-credits-and-usage/account_credits_usage_retrieve) |
| [Retrieve Enrichment Batch Results](actions/retrieve-enrichment-batch-results.md) | `GET /public/v1/enrichment/batch/:batch_id/` | [docs](https://docs.influencers.club/openapi/batch-enrichment/public_v1_enrichment_batch_retrieve) |
| [Retrieve Enrichment Batch Status](actions/retrieve-enrichment-batch-status.md) | `GET /public/v1/enrichment/batch/:batch_id/status/` | [docs](https://docs.influencers.club/openapi/batch-enrichment/public_v1_enrichment_batch_status_retrieve) |
| [Search Creators (Discovery)](actions/search-creators-discovery.md) | `POST /public/v1/discovery/` | [docs](https://docs.influencers.club/openapi/discovery-api/public_v1_discovery_create) |
