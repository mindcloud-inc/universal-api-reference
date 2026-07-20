# <img src="https://images.mindcloud.co/apps/icons/world-news-api-icon-square_1776182663099.png" alt="World News API logo" width="28" height="28"> World News API: Universal API

Access World News API for real-time and historical news search, top headlines, front pages, source discovery, article extraction, and geolocation utilities.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/worldNewsAPI/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://worldnewsapi.com
- **Vendor API docs:** https://worldnewsapi.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search News](actions/search-news.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worldNewsAPI/latest/actions/search-news?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [Search News Sources](actions/search-news-sources.md) | GET | Finds news sources in World News API by filter criteria. |
| [Suggest News Source](actions/suggest-news-source.md) | POST | Creates a news source suggestion in World News API. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Extract News](actions/extract-news.md) | GET | Extracts a news article from a URL using World News API. |
| [Extract News Links](actions/extract-news-links.md) | GET | Extracts news article links from a website using World News API. |
| [Get Geo Coordinates](actions/get-geo-coordinates.md) | GET | Retrieves geo coordinates for a location from World News API. |
| [Retrieve Front Page](actions/retrieve-front-page.md) | GET | Retrieves a newspaper front page from World News API. |
| [Retrieve News](actions/retrieve-news.md) | GET | Retrieves news articles from World News API by ID. |
| [Search News](actions/search-news.md) | GET | Finds news articles in World News API by filter criteria. |
| [Top News](actions/top-news.md) | GET | Retrieves top news headlines from World News API. |
| [Website to RSS Feed](actions/website-to-rss-feed.md) | GET | Converts a website to an RSS feed using World News API. |

