# <img src="https://images.mindcloud.co/apps/icons/scraping-dog_1775756940944.png" alt="ScrapingDog logo" width="28" height="28"> ScrapingDog: Universal API

ScrapingDog helps agents scrape webpages, search SERPs, and extract structured results across Google, Maps, News, Scholar, Amazon, YouTube, and other supported search surfaces.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scrapingDog/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.scrapingdog.com/
- **Vendor API docs:** https://docs.scrapingdog.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Details](actions/get-account-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves account details from ScrapingDog. |

### Ai Overview

| Action | Method | Description |
| --- | --- | --- |
| [Get Google AI Overview](actions/get-google-ai-overview.md) | GET | Retrieves Google AI Overview results through ScrapingDog. |

### Ai Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Google AI Mode](actions/get-google-ai-mode.md) | GET | Retrieves Google AI Mode results through ScrapingDog. |

### Author

| Action | Method | Description |
| --- | --- | --- |
| [Get Google Scholar Author](actions/get-google-scholar-author.md) | GET | Retrieves Google Scholar author details through ScrapingDog. |

### Citation

| Action | Method | Description |
| --- | --- | --- |
| [Get Google Scholar Author Citation](actions/get-google-scholar-author-citation.md) | GET | Retrieves Google Scholar author citations through ScrapingDog. |
| [Get Google Scholar Citation Formats](actions/get-google-scholar-citation-formats.md) | GET | Retrieves Google Scholar citation formats through ScrapingDog. |

### Finance Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Google Finance](actions/get-google-finance.md) | GET | Retrieves Google Finance data through ScrapingDog. |

### Flight

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Flights](actions/search-google-flights.md) | GET | Retrieves Google Flights search results through ScrapingDog. |

### Headline

| Action | Method | Description |
| --- | --- | --- |
| [Get Google News Headlines](actions/get-google-news-headlines.md) | GET | Retrieves Google News headlines through ScrapingDog. |

### Hotel

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Hotels](actions/search-google-hotels.md) | GET | Retrieves Google Hotels search results through ScrapingDog. |

### Image Match

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Lens](actions/search-google-lens.md) | GET | Retrieves Google Lens results through ScrapingDog. |

### Image Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Images](actions/search-google-images.md) | GET | Retrieves Google Images search results through ScrapingDog. |

### Job Posting

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Jobs](actions/search-google-jobs.md) | GET | Retrieves Google Jobs search results through ScrapingDog. |

### News Article

| Action | Method | Description |
| --- | --- | --- |
| [Search Google News](actions/search-google-news.md) | GET | Retrieves Google News search results through ScrapingDog. |

### Photo

| Action | Method | Description |
| --- | --- | --- |
| [List Google Maps Photos](actions/list-google-maps-photos.md) | GET | Retrieves Google Maps photos through ScrapingDog. |

### Place

| Action | Method | Description |
| --- | --- | --- |
| [Get Google Maps Place Details](actions/get-google-maps-place-details.md) | GET | Retrieves Google Maps place details through ScrapingDog. |
| [Search Google Local](actions/search-google-local.md) | GET | Retrieves Google Local search results through ScrapingDog. |
| [Search Google Maps](actions/search-google-maps.md) | GET | Retrieves Google Maps search results through ScrapingDog. |

### Post

| Action | Method | Description |
| --- | --- | --- |
| [List Google Maps Posts](actions/list-google-maps-posts.md) | GET | Retrieves Google Maps posts through ScrapingDog. |

### Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Amazon Product](actions/get-amazon-product.md) | GET | Retrieves Amazon product details through ScrapingDog. |
| [Get Google Product](actions/get-google-product.md) | GET | Retrieves Google product details through ScrapingDog. |
| [Search Amazon](actions/search-amazon.md) | GET | Retrieves Amazon search results through ScrapingDog. |
| [Search Google Shopping](actions/search-google-shopping.md) | GET | Retrieves Google Shopping search results through ScrapingDog. |

### Review

| Action | Method | Description |
| --- | --- | --- |
| [List Amazon Reviews](actions/list-amazon-reviews.md) | GET | Retrieves Amazon product reviews through ScrapingDog. |
| [List Google Maps Reviews](actions/list-google-maps-reviews.md) | GET | Retrieves Google Maps reviews through ScrapingDog. |

### Scholar Profile

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Scholar Profiles](actions/search-google-scholar-profiles.md) | GET | Retrieves Google Scholar profiles through ScrapingDog. |

### Scholar Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Scholar](actions/search-google-scholar.md) | GET | Retrieves Google Scholar search results through ScrapingDog. |

### Screenshot

| Action | Method | Description |
| --- | --- | --- |
| [Capture Screenshot](actions/capture-screenshot.md) | GET | Captures a webpage screenshot through ScrapingDog. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Universal Search](actions/run-universal-search.md) | GET | Retrieves universal search results through ScrapingDog. |
| [Search Bing](actions/search-bing.md) | GET | Retrieves Bing search results through ScrapingDog. |
| [Search DuckDuckGo](actions/search-duck-duck-go.md) | GET | Retrieves DuckDuckGo search results through ScrapingDog. |
| [Search Google](actions/search-google.md) | GET | Retrieves Google search results through ScrapingDog. |

### Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Google](actions/autocomplete-google.md) | GET | Retrieves Google autocomplete suggestions through ScrapingDog. |
| [Autocomplete Google Trends](actions/autocomplete-google-trends.md) | GET | Retrieves Google Trends autocomplete suggestions through ScrapingDog. |

### Transcript

| Action | Method | Description |
| --- | --- | --- |
| [Get YouTube Transcripts](actions/get-you-tube-transcripts.md) | GET | Retrieves YouTube transcripts through ScrapingDog. |

### Trend

| Action | Method | Description |
| --- | --- | --- |
| [List Google Trends Trending Now](actions/list-google-trends-trending-now.md) | GET | Retrieves trending-now topics from Google Trends through ScrapingDog. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Search YouTube](actions/search-you-tube.md) | GET | Retrieves YouTube search results through ScrapingDog. |

### Video Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Google Videos](actions/search-google-videos.md) | GET | Retrieves Google Videos search results through ScrapingDog. |

### Web Page

| Action | Method | Description |
| --- | --- | --- |
| [Post Through Scrape](actions/post-through-scrape.md) | GET | Sends a POST request through ScrapingDog. |
| [Scrape Web Page](actions/scrape-web-page.md) | GET | Retrieves webpage content through ScrapingDog. |

