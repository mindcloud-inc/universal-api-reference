# <img src="https://images.mindcloud.co/apps/icons/crawlbase_1776186574919.png" alt="Crawlbase logo" width="28" height="28"> Crawlbase: Universal API

Crawlbase provides crawling, scraping, screenshot, storage, account usage, and structured data extraction APIs for retrieving web data through Crawlbase infrastructure.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/crawlbase/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://crawlbase.com
- **Vendor API docs:** https://crawlbase.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Agents](actions/get-user-agents.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/crawlbase/latest/actions/get-user-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Usage](actions/get-account-usage.md) | GET | Retrieves account usage statistics from Crawlbase. |

### Airbnb Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Airbnb Search Results](actions/scrape-airbnb-search-results.md) | GET | Retrieves Airbnb search results from Crawlbase. |

### Aliexpress Product

| Action | Method | Description |
| --- | --- | --- |
| [Scrape AliExpress Product](actions/scrape-aliexpress-product.md) | GET | Retrieves AliExpress product data from Crawlbase. |

### Aliexpress Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Scrape AliExpress Search Results](actions/scrape-aliexpress-search-results.md) | GET | Retrieves AliExpress search results from Crawlbase. |

### Amazon Best Sellers

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Amazon Best Sellers](actions/scrape-amazon-best-sellers.md) | GET | Retrieves Amazon best-seller listings from Crawlbase. |

### Amazon New Releases

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Amazon New Releases](actions/scrape-amazon-new-releases.md) | GET | Retrieves Amazon new-release listings from Crawlbase. |

### Amazon Offer Listing

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Amazon Offer Listings](actions/scrape-amazon-offer-listings.md) | GET | Retrieves Amazon offer listings from Crawlbase. |

### Amazon Product Details

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Amazon Product Details](actions/scrape-amazon-product-details.md) | GET | Retrieves Amazon product details from Crawlbase. |

### Amazon Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Amazon Search Results](actions/scrape-amazon-search-results.md) | GET | Retrieves Amazon search results from Crawlbase. |

### Bestbuy Product Details

| Action | Method | Description |
| --- | --- | --- |
| [Scrape BestBuy Product Details](actions/scrape-bestbuy-product-details.md) | GET | Retrieves Best Buy product details from Crawlbase. |

### Bestbuy Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Scrape BestBuy Search Results](actions/scrape-bestbuy-search-results.md) | GET | Retrieves Best Buy search results from Crawlbase. |

### Bing Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Bing Search Results](actions/scrape-bing-search-results.md) | GET | Retrieves Bing search results from Crawlbase. |

### Crawled Page

| Action | Method | Description |
| --- | --- | --- |
| [Crawl URL](actions/crawl-url.md) | GET | Retrieves a crawled page from Crawlbase. |

### Ebay Product

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Ebay Product](actions/scrape-ebay-product.md) | GET | Retrieves eBay product data from Crawlbase. |

### Ebay Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Ebay Search Results](actions/scrape-ebay-search-results.md) | GET | Retrieves eBay search results from Crawlbase. |

### Ebay Seller Shop

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Ebay Seller Shop](actions/scrape-ebay-seller-shop.md) | GET | Retrieves an eBay seller shop from Crawlbase. |

### Eventbrite Event Details

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Eventbrite Event Details](actions/scrape-eventbrite-event-details.md) | GET | Retrieves Eventbrite event details from Crawlbase. |

### Eventbrite Events List

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Eventbrite Events List](actions/scrape-eventbrite-events-list.md) | GET | Retrieves Eventbrite event listings from Crawlbase. |

### Extracted Email

| Action | Method | Description |
| --- | --- | --- |
| [Extract Emails From Page](actions/extract-emails-from-page.md) | GET | Retrieves email addresses from a page with Crawlbase. |

### G2 Product Reviews

| Action | Method | Description |
| --- | --- | --- |
| [Scrape G2 Product Reviews](actions/scrape-g2-product-reviews.md) | GET | Retrieves G2 product reviews from Crawlbase. |

### Generic Extracted Content

| Action | Method | Description |
| --- | --- | --- |
| [Extract Generic Page Content](actions/extract-generic-page-content.md) | GET | Retrieves generic page content from Crawlbase. |

### Google Product Offers

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Google Product Offers](actions/scrape-google-product-offers.md) | GET | Retrieves Google product offers from Crawlbase. |

### Google Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Google Search Results](actions/scrape-google-search-results.md) | GET | Retrieves Google search results from Crawlbase. |

### Immobilienscout24 Property

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Immobilienscout24 Property](actions/scrape-immobilienscout24-property.md) | GET | Retrieves Immobilienscout24 property data from Crawlbase. |

### Linkedin Company

| Action | Method | Description |
| --- | --- | --- |
| [Scrape LinkedIn Company](actions/scrape-linkedin-company.md) | GET | Retrieves LinkedIn company data from Crawlbase. |

### Linkedin Feed

| Action | Method | Description |
| --- | --- | --- |
| [Scrape LinkedIn Feed](actions/scrape-linkedin-feed.md) | GET | Retrieves LinkedIn feed data from Crawlbase. |

### Linkedin Profile

| Action | Method | Description |
| --- | --- | --- |
| [Scrape LinkedIn Profile](actions/scrape-linkedin-profile.md) | GET | Retrieves a LinkedIn profile from Crawlbase. |

### Quora Question

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Quora Question](actions/scrape-quora-question.md) | GET | Retrieves Quora question data from Crawlbase. |

### Shein Product

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Shein Product](actions/scrape-shein-product.md) | GET | Retrieves Shein product data from Crawlbase. |

### Storage Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Storage Total Count](actions/get-storage-total-count.md) | GET | Retrieves the total storage item count from Crawlbase. |

### Storage Item

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Storage Bulk Items](actions/fetch-storage-bulk-items.md) | GET | Retrieves stored pages in bulk from Crawlbase. |
| [Get Storage Item](actions/get-storage-item.md) | GET | Retrieves a stored page from Crawlbase. |

### Storage Rid

| Action | Method | Description |
| --- | --- | --- |
| [List Storage RIDs](actions/list-storage-rids.md) | GET | Retrieves storage record IDs from Crawlbase. |

### Tiktok Product

| Action | Method | Description |
| --- | --- | --- |
| [Scrape TikTok Product](actions/scrape-tiktok-product.md) | GET | Retrieves TikTok product data from Crawlbase. |

### Tiktok Profile

| Action | Method | Description |
| --- | --- | --- |
| [Scrape TikTok Profile](actions/scrape-tiktok-profile.md) | GET | Retrieves a TikTok profile from Crawlbase. |

### Tiktok Shop

| Action | Method | Description |
| --- | --- | --- |
| [Scrape TikTok Shop](actions/scrape-tiktok-shop.md) | GET | Retrieves TikTok shop data from Crawlbase. |

### User Agent

| Action | Method | Description |
| --- | --- | --- |
| [Get User Agents](actions/get-user-agents.md) | GET | Retrieves random user-agent strings from Crawlbase. |

### Walmart Category

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Walmart Category](actions/scrape-walmart-category.md) | GET | Retrieves Walmart category data from Crawlbase. |

### Walmart Product Details

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Walmart Product Details](actions/scrape-walmart-product-details.md) | GET | Retrieves Walmart product details from Crawlbase. |

### Walmart Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Scrape Walmart Search Results](actions/scrape-walmart-search-results.md) | GET | Retrieves Walmart search results from Crawlbase. |

