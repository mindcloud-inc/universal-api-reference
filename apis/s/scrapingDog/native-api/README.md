# ScrapingDog: Native API Reference

A consolidated summary of ScrapingDog's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.scrapingdog.com/
- **API base URL:** `https://api.scrapingdog.com`

## Authentication

### API Key

Use your ScrapingDog API key. MindCloud sends it as the api_key query parameter on requests to api.scrapingdog.com.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.scrapingdog.com/web-scraping-api)

## API conventions

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Autocomplete Google](actions/autocomplete-google.md) | `GET /google_autocomplete` | [docs](https://docs.scrapingdog.com/google-autocomplete-api) |
| [Autocomplete Google Trends](actions/autocomplete-google-trends.md) | `GET /google_trends/autocomplete` | [docs](https://docs.scrapingdog.com/google-trends-api/google-trends-autocomplete-api) |
| [Capture Screenshot](actions/capture-screenshot.md) | `GET /screenshot` | [docs](https://docs.scrapingdog.com/screenshot-api) |
| [Get Account Details](actions/get-account-details.md) | `GET /account` | [docs](https://docs.scrapingdog.com/account-api) |
| [Get Amazon Product](actions/get-amazon-product.md) | `GET /amazon/product` | [docs](https://docs.scrapingdog.com/amazon-scraper-api/amazon-product-scraper) |
| [Get Google AI Mode](actions/get-google-ai-mode.md) | `GET /google/ai_mode` | [docs](https://docs.scrapingdog.com/google-ai-mode-api) |
| [Get Google AI Overview](actions/get-google-ai-overview.md) | `GET /google/ai_overview` | [docs](https://docs.scrapingdog.com/google-ai-overview-api) |
| [Get Google Finance](actions/get-google-finance.md) | `GET /google_finance` | [docs](https://docs.scrapingdog.com/google-finance-api) |
| [Get Google Maps Place Details](actions/get-google-maps-place-details.md) | `GET /google_maps/places` | [docs](https://docs.scrapingdog.com/google-maps-api/google-maps-places-api) |
| [Get Google News Headlines](actions/get-google-news-headlines.md) | `GET /google_news/v2` | [docs](https://docs.scrapingdog.com/google-news-scraper-apis/google-news-api) |
| [Get Google Product](actions/get-google-product.md) | `GET /google_product` | [docs](https://docs.scrapingdog.com/google-product-api) |
| [Get Google Scholar Author](actions/get-google-scholar-author.md) | `GET /google_scholar/author` | [docs](https://docs.scrapingdog.com/google-scholar-api/google-scholar-author-api) |
| [Get Google Scholar Author Citation](actions/get-google-scholar-author-citation.md) | `GET /google_scholar/author` | [docs](https://docs.scrapingdog.com/google-scholar-api/google-scholar-author-api/google-scholar-author-citation-api) |
| [Get Google Scholar Citation Formats](actions/get-google-scholar-citation-formats.md) | `GET /google_scholar/cite` | [docs](https://docs.scrapingdog.com/google-scholar-api/google-scholar-cite-api) |
| [Get YouTube Transcripts](actions/get-you-tube-transcripts.md) | `GET /youtube/transcripts` | [docs](https://docs.scrapingdog.com/youtube-scraper-api/youtube-transcripts-api) |
| [List Amazon Reviews](actions/list-amazon-reviews.md) | `GET /amazon/reviews` | [docs](https://docs.scrapingdog.com/amazon-scraper-api/amazon-reviews-api) |
| [List Google Maps Photos](actions/list-google-maps-photos.md) | `GET /google_maps/photos` | [docs](https://docs.scrapingdog.com/google-maps-api/google-maps-photos-api) |
| [List Google Maps Posts](actions/list-google-maps-posts.md) | `GET /google_maps/posts` | [docs](https://docs.scrapingdog.com/google-maps-api/google-maps-posts-api) |
| [List Google Maps Reviews](actions/list-google-maps-reviews.md) | `GET /google_maps/reviews` | [docs](https://docs.scrapingdog.com/google-maps-api/google-maps-reviews-api) |
| [List Google Trends Trending Now](actions/list-google-trends-trending-now.md) | `GET /google_trends/trending_now` | [docs](https://docs.scrapingdog.com/google-trends-api/google-trends-trending-now-api) |
| [Post Through Scrape](actions/post-through-scrape.md) | `POST /scrape` | [docs](https://docs.scrapingdog.com/post-request) |
| [Run Universal Search](actions/run-universal-search.md) | `GET /search` | [docs](https://docs.scrapingdog.com/universal-search-api) |
| [Scrape Web Page](actions/scrape-web-page.md) | `GET /scrape` | [docs](https://docs.scrapingdog.com/web-scraping-api) |
| [Search Amazon](actions/search-amazon.md) | `GET /amazon/search` | [docs](https://docs.scrapingdog.com/amazon-scraper-api/amazon-search-scraper) |
| [Search Bing](actions/search-bing.md) | `GET /bing/search` | [docs](https://docs.scrapingdog.com/bing-search-scraper-api) |
| [Search DuckDuckGo](actions/search-duck-duck-go.md) | `GET /duckduckgo/search` | [docs](https://docs.scrapingdog.com/duckduckgo-scraper-api/duckduckgo-search-api) |
| [Search Google](actions/search-google.md) | `GET /google` | [docs](https://docs.scrapingdog.com/google-search-scraper-api) |
| [Search Google Flights](actions/search-google-flights.md) | `GET /google_flights` | [docs](https://docs.scrapingdog.com/google-flights-api) |
| [Search Google Hotels](actions/search-google-hotels.md) | `GET /google_hotels` | [docs](https://docs.scrapingdog.com/google-hotels-api) |
| [Search Google Images](actions/search-google-images.md) | `GET /google_images` | [docs](https://docs.scrapingdog.com/google-images-api) |
| [Search Google Jobs](actions/search-google-jobs.md) | `GET /google_jobs` | [docs](https://docs.scrapingdog.com/google-jobs-api) |
| [Search Google Lens](actions/search-google-lens.md) | `GET /google_lens` | [docs](https://docs.scrapingdog.com/google-lens-api) |
| [Search Google Local](actions/search-google-local.md) | `GET /google_local` | [docs](https://docs.scrapingdog.com/google-local-api) |
| [Search Google Maps](actions/search-google-maps.md) | `GET /google_maps` | [docs](https://docs.scrapingdog.com/google-maps-api/google-maps-search-api) |
| [Search Google News](actions/search-google-news.md) | `GET /google_news` | [docs](https://docs.scrapingdog.com/google-news-scraper-apis/google-news-search-api) |
| [Search Google Scholar](actions/search-google-scholar.md) | `GET /google_scholar` | [docs](https://docs.scrapingdog.com/google-scholar-api) |
| [Search Google Scholar Profiles](actions/search-google-scholar-profiles.md) | `GET /google_scholar/profiles` | [docs](https://docs.scrapingdog.com/google-scholar-api/google-scholar-profiles-api) |
| [Search Google Shopping](actions/search-google-shopping.md) | `GET /google_shopping` | [docs](https://docs.scrapingdog.com/google-shopping-api) |
| [Search Google Videos](actions/search-google-videos.md) | `GET /google_videos` | [docs](https://docs.scrapingdog.com/google-videos-api) |
| [Search YouTube](actions/search-you-tube.md) | `GET /youtube/search` | [docs](https://docs.scrapingdog.com/youtube-scraper-api/youtube-search-api) |
