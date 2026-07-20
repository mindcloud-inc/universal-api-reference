# Oxylabs: Native API Reference

A consolidated summary of Oxylabs's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.oxylabs.io/scraping-solutions/web-scraper-api
- **API base URL:** `https://realtime.oxylabs.io`

## Authentication

### Basic Authentication

Use your Oxylabs API-user username and password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developers.oxylabs.io/help-center/getting-started/start-using-web-scraper-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Ask ChatGPT](actions/ask-chatgpt.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/chatgpt) |
| [Ask Google AI Mode](actions/ask-google-ai-mode.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/google/ai-mode) |
| [Ask Perplexity](actions/ask-perplexity.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/perplexity) |
| [Browse Target Category](actions/browse-target-category.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/north-american-e-commerce/target/category) |
| [Check YouTube Trainability](actions/check-youtube-trainability.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/youtube/youtube-video-trainability) |
| [Explore Google Trends](actions/explore-google-trends.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/google/trends-explore) |
| [Fetch Universal URL](actions/fetch-universal-url.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/generic-target) |
| [Get Amazon Best Sellers](actions/get-amazon-best-sellers.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/amazon/best-sellers) |
| [Get Amazon Pricing](actions/get-amazon-pricing.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/amazon/pricing) |
| [Get Amazon Product](actions/get-amazon-product.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/amazon/product) |
| [Get Amazon Seller](actions/get-amazon-seller.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/amazon/sellers) |
| [Get Best Buy Product](actions/get-best-buy-product.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/north-american-e-commerce/bestbuy/product) |
| [Get eBay Product](actions/get-ebay-product.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/ebay/product) |
| [Get Etsy Product](actions/get-etsy-product.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/etsy/product) |
| [Get Google Shopping Product](actions/get-google-shopping-product.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/google/shopping/shopping-product) |
| [Get Instacart Product](actions/get-instacart-product.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/north-american-e-commerce/instacart/product) |
| [Get Target Product](actions/get-target-product.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/north-american-e-commerce/target/product) |
| [Get Walmart Product](actions/get-walmart-product.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/walmart/product) |
| [Get YouTube Channel](actions/get-youtube-channel.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/youtube/youtube-channel) |
| [Get YouTube Metadata](actions/get-youtube-metadata.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/youtube/youtube-metadata) |
| [Get YouTube Subtitles](actions/get-youtube-subtitles.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/youtube/youtube-subtitles) |
| [Get YouTube Suggestions](actions/get-youtube-suggestions.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/youtube/autocomplete) |
| [Get YouTube Transcript](actions/get-youtube-transcript.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/youtube/youtube-transcript) |
| [Search Amazon](actions/search-amazon.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/amazon/search) |
| [Search Best Buy](actions/search-best-buy.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/north-american-e-commerce/bestbuy/search) |
| [Search Bing](actions/search-bing.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/bing/search) |
| [Search eBay](actions/search-ebay.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/ebay/search) |
| [Search Etsy](actions/search-etsy.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/etsy/search) |
| [Search Google Ads](actions/search-google-ads.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/google/ads) |
| [Search Google Images](actions/search-google-images.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/google/search/image-search) |
| [Search Google Lens](actions/search-google-lens.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/google/lens) |
| [Search Google Local](actions/search-google-local.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/google/search/local-search) |
| [Search Google News](actions/search-google-news.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/google/search/news-search) |
| [Search Google Shopping](actions/search-google-shopping.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/google/shopping/shopping-search) |
| [Search Google Travel Hotels](actions/search-google-travel-hotels.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/google/travel-hotels) |
| [Search Google Web](actions/search-google-web.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/google/search/search) |
| [Search Instacart](actions/search-instacart.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/north-american-e-commerce/instacart/search) |
| [Search Target](actions/search-target.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/north-american-e-commerce/target/search) |
| [Search Walmart](actions/search-walmart.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/walmart/search) |
| [Search YouTube](actions/search-youtube.md) | `POST /v1/queries` | [docs](https://developers.oxylabs.io/scraping-solutions/web-scraper-api/targets/youtube/youtube-search) |
