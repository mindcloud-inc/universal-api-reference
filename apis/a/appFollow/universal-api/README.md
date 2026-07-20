# <img src="https://images.mindcloud.co/apps/icons/app-follow_1773870271285.png" alt="AppFollow logo" width="28" height="28"> AppFollow: Universal API

Reply to reviews and track ratings, rankings, keywords, and app updates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/appFollow/latest
- **Category:** Marketing
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://appfollow.io
- **Vendor API docs:** https://docs.api.appfollow.io/reference/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List App Collections](actions/list-app-collections.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appFollow/latest/actions/list-app-collections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Asosearchresult

| Action | Method | Description |
| --- | --- | --- |
| [Search ASO](actions/search-aso.md) | GET | Retrieves ASO search results from AppFollow. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [List App Collections](actions/list-app-collections.md) | GET | Retrieves app collections from AppFollow. |

### Collectionapp

| Action | Method | Description |
| --- | --- | --- |
| [List Collection Apps](actions/list-collection-apps.md) | GET | Retrieves apps from an AppFollow collection. |

### Featuredreview

| Action | Method | Description |
| --- | --- | --- |
| [List Featured Reviews](actions/list-featured-reviews.md) | GET | Retrieves featured reviews from AppFollow. |

### Keyword

| Action | Method | Description |
| --- | --- | --- |
| [List Keywords](actions/list-keywords.md) | GET | Retrieves keyword data from AppFollow. |

### Keywordsuggestion

| Action | Method | Description |
| --- | --- | --- |
| [Get Keyword Suggestions](actions/get-keyword-suggestions.md) | GET | Retrieves keyword suggestions from AppFollow. |

### Ranking

| Action | Method | Description |
| --- | --- | --- |
| [List Rankings](actions/list-rankings.md) | GET | Retrieves app rankings from AppFollow. |

### Ratinghistory

| Action | Method | Description |
| --- | --- | --- |
| [Get Ratings History](actions/get-ratings-history.md) | GET | Retrieves ratings history from AppFollow. |

### Review

| Action | Method | Description |
| --- | --- | --- |
| [List Reviews](actions/list-reviews.md) | GET | Retrieves filtered app reviews from AppFollow. |

### Reviewratingstat

| Action | Method | Description |
| --- | --- | --- |
| [Get Review Rating Stats](actions/get-review-rating-stats.md) | GET | Retrieves review rating statistics from AppFollow. |

### Reviewreplycount

| Action | Method | Description |
| --- | --- | --- |
| [Get Review Reply Counts](actions/get-review-reply-counts.md) | GET | Retrieves review reply counts from AppFollow. |

### Reviewreplyspeed

| Action | Method | Description |
| --- | --- | --- |
| [Get Review Reply Speed](actions/get-review-reply-speed.md) | GET | Retrieves review reply speed statistics from AppFollow. |

### Reviewreplystat

| Action | Method | Description |
| --- | --- | --- |
| [Get Review Reply Stats](actions/get-review-reply-stats.md) | GET | Retrieves review reply statistics from AppFollow. |

### Reviewstat

| Action | Method | Description |
| --- | --- | --- |
| [Get Review Stats](actions/get-review-stats.md) | GET | Retrieves review statistics from AppFollow. |

### Reviewsummary

| Action | Method | Description |
| --- | --- | --- |
| [Get Review Summary](actions/get-review-summary.md) | GET | Retrieves a review summary from AppFollow. |

### Topchartentry

| Action | Method | Description |
| --- | --- | --- |
| [List Top Charts](actions/list-top-charts.md) | GET | Retrieves top chart results from AppFollow. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from AppFollow. |

### Version

| Action | Method | Description |
| --- | --- | --- |
| [List Versions](actions/list-versions.md) | GET | Retrieves app version changes from AppFollow. |

### Versionnote

| Action | Method | Description |
| --- | --- | --- |
| [List New Versions](actions/list-new-versions.md) | GET | Retrieves new version details from AppFollow. |

