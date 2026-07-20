# <img src="https://images.mindcloud.co/apps/icons/oxylabs_1775668337428.png" alt="Oxylabs logo" width="28" height="28"> Oxylabs: Universal API

Oxylabs: Scrape search, shopping, video, and web data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/oxylabs/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://oxylabs.io/products/scraper-api/web
- **Vendor API docs:** https://developers.oxylabs.io/scraping-solutions/web-scraper-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Google Web](actions/search-google-web.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oxylabs/latest/actions/search-google-web?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Ai

| Action | Method | Description |
| --- | --- | --- |
| [Ask ChatGPT](actions/ask-chatgpt.md) | GET | Retrieves ChatGPT prompt responses with Oxylabs. |
| [Ask Perplexity](actions/ask-perplexity.md) | GET | Retrieves Perplexity prompt responses with Oxylabs. |

### Amazon

| Action | Method | Description |
| --- | --- | --- |
| [Get Amazon Best Sellers](actions/get-amazon-best-sellers.md) | GET | Retrieves Amazon Best Sellers data with Oxylabs. |
| [Get Amazon Pricing](actions/get-amazon-pricing.md) | GET | Retrieves Amazon pricing data with Oxylabs. |
| [Get Amazon Product](actions/get-amazon-product.md) | GET | Retrieves Amazon product details with Oxylabs. |
| [Get Amazon Seller](actions/get-amazon-seller.md) | GET | Retrieves Amazon seller details with Oxylabs. |
| [Search Amazon](actions/search-amazon.md) | GET | Searches Amazon product results with Oxylabs. |

### Best Buy

| Action | Method | Description |
| --- | --- | --- |
| [Get Best Buy Product](actions/get-best-buy-product.md) | GET | Retrieves Best Buy product details with Oxylabs. |
| [Search Best Buy](actions/search-best-buy.md) | GET | Searches Best Buy product results with Oxylabs. |

### Bing

| Action | Method | Description |
| --- | --- | --- |
| [Search Bing](actions/search-bing.md) | GET | Searches Bing web results with Oxylabs. |

### Ebay

| Action | Method | Description |
| --- | --- | --- |
| [Get eBay Product](actions/get-ebay-product.md) | GET | Retrieves eBay product details with Oxylabs. |
| [Search eBay](actions/search-ebay.md) | GET | Searches eBay product results with Oxylabs. |

### Etsy

| Action | Method | Description |
| --- | --- | --- |
| [Get Etsy Product](actions/get-etsy-product.md) | GET | Retrieves Etsy product details with Oxylabs. |
| [Search Etsy](actions/search-etsy.md) | GET | Searches Etsy product results with Oxylabs. |

### Google

| Action | Method | Description |
| --- | --- | --- |
| [Ask Google AI Mode](actions/ask-google-ai-mode.md) | GET | Retrieves Google AI Mode responses with Oxylabs. |
| [Explore Google Trends](actions/explore-google-trends.md) | GET | Retrieves Google Trends data with Oxylabs. |
| [Get Google Shopping Product](actions/get-google-shopping-product.md) | GET | Retrieves Google Shopping product details with Oxylabs. |
| [Search Google Ads](actions/search-google-ads.md) | GET | Searches Google ad results with Oxylabs. |
| [Search Google Images](actions/search-google-images.md) | GET | Searches Google image results with Oxylabs. |
| [Search Google Lens](actions/search-google-lens.md) | GET | Searches Google Lens results with Oxylabs. |
| [Search Google Local](actions/search-google-local.md) | GET | Searches Google local results with Oxylabs. |
| [Search Google News](actions/search-google-news.md) | GET | Searches Google News results with Oxylabs. |
| [Search Google Shopping](actions/search-google-shopping.md) | GET | Searches Google Shopping results with Oxylabs. |
| [Search Google Travel Hotels](actions/search-google-travel-hotels.md) | GET | Searches Google Travel hotel listings with Oxylabs. |
| [Search Google Web](actions/search-google-web.md) | GET | Searches Google web results with Oxylabs. |

### Instacart

| Action | Method | Description |
| --- | --- | --- |
| [Get Instacart Product](actions/get-instacart-product.md) | GET | Retrieves Instacart product details with Oxylabs. |
| [Search Instacart](actions/search-instacart.md) | GET | Searches Instacart product results with Oxylabs. |

### Target

| Action | Method | Description |
| --- | --- | --- |
| [Browse Target Category](actions/browse-target-category.md) | GET | Retrieves Target category listings with Oxylabs. |
| [Get Target Product](actions/get-target-product.md) | GET | Retrieves Target product details with Oxylabs. |
| [Search Target](actions/search-target.md) | GET | Searches Target product results with Oxylabs. |

### Universal

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Universal URL](actions/fetch-universal-url.md) | GET | Retrieves data from any public URL with Oxylabs. |

### Walmart

| Action | Method | Description |
| --- | --- | --- |
| [Get Walmart Product](actions/get-walmart-product.md) | GET | Retrieves Walmart product details with Oxylabs. |
| [Search Walmart](actions/search-walmart.md) | GET | Searches Walmart product results with Oxylabs. |

### Youtube

| Action | Method | Description |
| --- | --- | --- |
| [Check YouTube Trainability](actions/check-youtube-trainability.md) | GET | Checks YouTube AI training permission status with Oxylabs. |
| [Get YouTube Channel](actions/get-youtube-channel.md) | GET | Retrieves YouTube channel data with Oxylabs. |
| [Get YouTube Metadata](actions/get-youtube-metadata.md) | GET | Retrieves YouTube video metadata with Oxylabs. |
| [Get YouTube Subtitles](actions/get-youtube-subtitles.md) | GET | Retrieves YouTube subtitles data with Oxylabs. |
| [Get YouTube Suggestions](actions/get-youtube-suggestions.md) | GET | Retrieves YouTube search suggestions with Oxylabs. |
| [Get YouTube Transcript](actions/get-youtube-transcript.md) | GET | Retrieves YouTube transcript data with Oxylabs. |
| [Search YouTube](actions/search-youtube.md) | GET | Searches YouTube search results with Oxylabs. |

