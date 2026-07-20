# <img src="https://images.mindcloud.co/apps/icons/insight-iq_1776089753480.png" alt="InsightIQ logo" width="28" height="28"> InsightIQ: Universal API

Creator intelligence API for work-platform connections, creator discovery, public-content analytics, safety screening, trends, and webhook-driven data workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/insightIQ/latest
- **Category:** Marketing
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://insightiq.ai
- **Vendor API docs:** https://docs.insightiq.ai/docs/api-reference/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Work Platforms](actions/list-work-platforms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/list-work-platforms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Connection Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Connection Link](actions/create-connection-link.md) | POST | Creates a new connection link in InsightIQ. |

### Content Comments Fetch Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Async Content Comments Fetch](actions/create-async-content-comments-fetch.md) | POST | Creates an async content comments fetch request in InsightIQ. |

### Content Comments Fetch Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Async Content Comments Fetch](actions/get-async-content-comments-fetch.md) | GET | Retrieves an async content comments result from InsightIQ. |

### Creator Brand

| Action | Method | Description |
| --- | --- | --- |
| [List Creator Brands](actions/list-creator-brands.md) | GET | Retrieves available creator brands from InsightIQ. |

### Creator Contact Info

| Action | Method | Description |
| --- | --- | --- |
| [Get Creator Contact Info](actions/get-creator-contact-info.md) | GET | Retrieves creator contact information from InsightIQ. |

### Creator Content

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Public Creator Content](actions/fetch-public-creator-content.md) | GET | Retrieves public creator content from InsightIQ. |

### Creator Interest

| Action | Method | Description |
| --- | --- | --- |
| [List Creator Interests](actions/list-creator-interests.md) | GET | Retrieves available creator interests from InsightIQ. |

### Creator Language

| Action | Method | Description |
| --- | --- | --- |
| [List Creator Languages](actions/list-creator-languages.md) | GET | Retrieves available creator languages from InsightIQ. |

### Creator Location

| Action | Method | Description |
| --- | --- | --- |
| [List Creator Locations](actions/list-creator-locations.md) | GET | Finds creator locations in InsightIQ by substring. |

### Creator Profile Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Creator Profile Analytics](actions/get-creator-profile-analytics.md) | GET | Retrieves creator profile analytics from InsightIQ. |

### Creator Profile Analytics Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Async Creator Profile Analytics](actions/get-async-creator-profile-analytics.md) | GET | Retrieves an async creator analytics result from InsightIQ. |

### Creator Profile Analytics Request

| Action | Method | Description |
| --- | --- | --- |
| [Create Async Creator Profile Analytics](actions/create-async-creator-profile-analytics.md) | POST | Creates an async creator analytics request in InsightIQ. |

### Creator Topic

| Action | Method | Description |
| --- | --- | --- |
| [Search Creator Topics](actions/search-creator-topics.md) | GET | Finds creator topics in InsightIQ by keyword. |

### Creator Topic Relevance

| Action | Method | Description |
| --- | --- | --- |
| [Get Creator Topic Relevance](actions/get-creator-topic-relevance.md) | GET | Retrieves creator topic relevance from InsightIQ. |

### Education Degree

| Action | Method | Description |
| --- | --- | --- |
| [List Professional Education Degrees](actions/list-professional-education-degrees.md) | GET | Finds education degrees in InsightIQ by substring. |

### Education Institute

| Action | Method | Description |
| --- | --- | --- |
| [List Professional Education Institutes](actions/list-professional-education-institutes.md) | GET | Finds education institutes in InsightIQ by substring. |

### Flagging Criteria

| Action | Method | Description |
| --- | --- | --- |
| [List Flagging Criteria](actions/list-flagging-criteria.md) | GET | Retrieves available flagging criteria from InsightIQ. |

### Media Safety Screening

| Action | Method | Description |
| --- | --- | --- |
| [Create Media Safety Screening](actions/create-media-safety-screening.md) | POST | Creates a media safety screening in InsightIQ. |
| [Get Media Safety Screening](actions/get-media-safety-screening.md) | GET | Retrieves a media safety screening from InsightIQ. |

### Professional Company

| Action | Method | Description |
| --- | --- | --- |
| [List Professional Companies](actions/list-professional-companies.md) | GET | Finds professional companies in InsightIQ by substring. |

### Professional Location

| Action | Method | Description |
| --- | --- | --- |
| [List Professional Locations](actions/list-professional-locations.md) | GET | Finds professional locations in InsightIQ by substring. |

### Professional Topic

| Action | Method | Description |
| --- | --- | --- |
| [List Professional Topics](actions/list-professional-topics.md) | GET | Finds professional topics in InsightIQ by keyword. |

### Sdk Token

| Action | Method | Description |
| --- | --- | --- |
| [Create SDK Token](actions/create-sdk-token.md) | POST | Creates a new SDK token in InsightIQ. |

### Talks About Topic

| Action | Method | Description |
| --- | --- | --- |
| [List Professional Talks About](actions/list-professional-talks-about.md) | GET | Finds talks-about topics in InsightIQ by substring. |

### Trending Creator

| Action | Method | Description |
| --- | --- | --- |
| [Get Trending Creators](actions/get-trending-creators.md) | GET | Retrieves current trending creators from InsightIQ. |

### Trending Hashtag

| Action | Method | Description |
| --- | --- | --- |
| [Get Trending Hashtags](actions/get-trending-hashtags.md) | GET | Retrieves current trending hashtags from InsightIQ. |

### Trending Video

| Action | Method | Description |
| --- | --- | --- |
| [Get Trending Videos](actions/get-trending-videos.md) | GET | Retrieves current trending videos from InsightIQ. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Create User](actions/create-user.md) | POST | Creates a new user in InsightIQ. |
| [Get User](actions/get-user.md) | GET | Retrieves a single user from InsightIQ. |
| [Get User By External ID](actions/get-user-by-external-id.md) | GET | Finds a user in InsightIQ by external ID. |
| [List Users](actions/list-users.md) | GET | Retrieves a list of users from InsightIQ. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in InsightIQ. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from InsightIQ. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a single webhook from InsightIQ. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves a list of webhooks from InsightIQ. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in InsightIQ. |

### Work Platform

| Action | Method | Description |
| --- | --- | --- |
| [Get Work Platform](actions/get-work-platform.md) | GET | Retrieves a work platform from InsightIQ. |
| [List Work Platforms](actions/list-work-platforms.md) | GET | Retrieves available work platforms from InsightIQ. |

