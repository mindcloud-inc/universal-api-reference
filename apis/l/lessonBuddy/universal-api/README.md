# <img src="https://images.mindcloud.co/apps/icons/1706354457372_1776955750452.jpeg" alt="LessonBuddy logo" width="28" height="28"> LessonBuddy: Universal API

Public API for Big Blue Swim School's LessonBuddy platform, covering documented campaign, family, inventory, and location endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lessonBuddy/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://bigblueswimschool.com
- **Vendor API docs:** https://www.postman.com/bigblueswimschool/documentation/4169241-f58a8184-3099-4d87-9da8-9bd2639880a8

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Published Locations](actions/list-published-locations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lessonBuddy/latest/actions/list-published-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Active Campaign](actions/get-active-campaign.md) | GET | Retrieves the active campaign for a location in LessonBuddy. |

### Inventory Price

| Action | Method | Description |
| --- | --- | --- |
| [Get Price By SKU](actions/get-price-by-sku.md) | GET | Retrieves a product price in LessonBuddy by SKU. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in LessonBuddy. |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Closest Locations](actions/get-closest-locations.md) | GET | Finds locations in LessonBuddy by distance from coordinates. |
| [Get Location By ID](actions/get-location-by-id.md) | GET | Retrieves a location from LessonBuddy by ID. |
| [Get Location By Slug](actions/get-location-by-slug.md) | GET | Retrieves a location from LessonBuddy by slug. |
| [List Published Locations](actions/list-published-locations.md) | GET | Retrieves published locations from LessonBuddy. |
| [Search Locations](actions/search-locations.md) | GET | Finds locations in LessonBuddy near an address. |

### Location Province Group

| Action | Method | Description |
| --- | --- | --- |
| [List Published Locations By Province](actions/list-published-locations-by-province.md) | GET | Retrieves published locations grouped by province in LessonBuddy. |

### Referral Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Referral Info](actions/get-referral-info.md) | GET | Retrieves referral bonus information for a family in LessonBuddy. |

### Utm Code

| Action | Method | Description |
| --- | --- | --- |
| [Get UTM Code](actions/get-utm-code.md) | GET | Finds a UTM code in LessonBuddy by tracking parameters. |

