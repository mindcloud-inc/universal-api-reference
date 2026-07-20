# Crawlbase: Native API Reference

A consolidated summary of Crawlbase's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://crawlbase.com/docs/
- **API base URL:** `https://api.crawlbase.com`

## Authentication

### API Key

Crawlbase API key token sent as the token query parameter.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://crawlbase.com/docs/crawling-api/parameters/)

## API conventions

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Crawl URL](actions/crawl-url.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/parameters/) |
| [Extract Emails From Page](actions/extract-emails-from-page.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Extract Generic Page Content](actions/extract-generic-page-content.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Fetch Storage Bulk Items](actions/fetch-storage-bulk-items.md) | `POST /storage/bulk` | [docs](https://crawlbase.com/docs/cloud-storage/bulk/) |
| [Get Account Usage](actions/get-account-usage.md) | `GET /account` | [docs](https://crawlbase.com/docs/account-api/) |
| [Get Storage Item](actions/get-storage-item.md) | `GET /storage` | [docs](https://crawlbase.com/docs/cloud-storage/parameters/) |
| [Get Storage Total Count](actions/get-storage-total-count.md) | `GET /storage/total_count` | [docs](https://crawlbase.com/docs/cloud-storage/total-count/) |
| [Get User Agents](actions/get-user-agents.md) | `GET /user_agents` | [docs](https://crawlbase.com/docs/user-agents-api/parameters/) |
| [List Storage RIDs](actions/list-storage-rids.md) | `GET /storage/rids` | [docs](https://crawlbase.com/docs/cloud-storage/rids/) |
| [Scrape Airbnb Search Results](actions/scrape-airbnb-search-results.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape AliExpress Product](actions/scrape-aliexpress-product.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape AliExpress Search Results](actions/scrape-aliexpress-search-results.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Amazon Best Sellers](actions/scrape-amazon-best-sellers.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Amazon New Releases](actions/scrape-amazon-new-releases.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Amazon Offer Listings](actions/scrape-amazon-offer-listings.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Amazon Product Details](actions/scrape-amazon-product-details.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Amazon Search Results](actions/scrape-amazon-search-results.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape BestBuy Product Details](actions/scrape-bestbuy-product-details.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape BestBuy Search Results](actions/scrape-bestbuy-search-results.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Bing Search Results](actions/scrape-bing-search-results.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Ebay Product](actions/scrape-ebay-product.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Ebay Search Results](actions/scrape-ebay-search-results.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Ebay Seller Shop](actions/scrape-ebay-seller-shop.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Eventbrite Event Details](actions/scrape-eventbrite-event-details.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Eventbrite Events List](actions/scrape-eventbrite-events-list.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape G2 Product Reviews](actions/scrape-g2-product-reviews.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Google Product Offers](actions/scrape-google-product-offers.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Google Search Results](actions/scrape-google-search-results.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Immobilienscout24 Property](actions/scrape-immobilienscout24-property.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape LinkedIn Company](actions/scrape-linkedin-company.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape LinkedIn Feed](actions/scrape-linkedin-feed.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape LinkedIn Profile](actions/scrape-linkedin-profile.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Quora Question](actions/scrape-quora-question.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Shein Product](actions/scrape-shein-product.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape TikTok Product](actions/scrape-tiktok-product.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape TikTok Profile](actions/scrape-tiktok-profile.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape TikTok Shop](actions/scrape-tiktok-shop.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Walmart Category](actions/scrape-walmart-category.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Walmart Product Details](actions/scrape-walmart-product-details.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
| [Scrape Walmart Search Results](actions/scrape-walmart-search-results.md) | `GET /` | [docs](https://crawlbase.com/docs/crawling-api/scrapers/) |
