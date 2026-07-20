# LessonBuddy: Native API Reference

A consolidated summary of LessonBuddy's API configuration and 11 documented operations, with links to official documentation.

- **Official docs:** https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8
- **API base URL:** `https://api.lessonbuddy.com`

## Authentication

### Public API

No authentication is required for the documented public LessonBuddy API endpoints.

This API does not require request authentication.

[Official authentication documentation](https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (11 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | `POST /v2/campaign/leads` | [docs](https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8) |
| [Get Active Campaign](actions/get-active-campaign.md) | `GET /v2/campaign/campaigns/location/:locationId/active` | [docs](https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8) |
| [Get Closest Locations](actions/get-closest-locations.md) | `GET /v2/location/locations/closest/:latitude/:longitude/:radius` | [docs](https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8) |
| [Get Location By ID](actions/get-location-by-id.md) | `GET /v2/location/locations/:id` | [docs](https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8) |
| [Get Location By Slug](actions/get-location-by-slug.md) | `GET /v2/location/locations/slug/:slug` | [docs](https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8) |
| [Get Price By SKU](actions/get-price-by-sku.md) | `GET /v2/ims/inventory/:locationId/price-by-sku/:sku` | [docs](https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8) |
| [Get Referral Info](actions/get-referral-info.md) | `GET /v2/family/families/referral-info/:familyId` | [docs](https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8) |
| [Get UTM Code](actions/get-utm-code.md) | `GET /v2/campaign/utm-codes` | [docs](https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8) |
| [List Published Locations](actions/list-published-locations.md) | `GET /v2/location/locations/published` | [docs](https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8) |
| [List Published Locations By Province](actions/list-published-locations-by-province.md) | `GET /v2/location/locations/published/by-province` | [docs](https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8) |
| [Search Locations](actions/search-locations.md) | `POST /v2/location/locations/search` | [docs](https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8) |
