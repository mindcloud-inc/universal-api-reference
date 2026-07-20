# <img src="https://images.mindcloud.co/apps/icons/scraping-bot_1776174991882.png" alt="ScrapingBot logo" width="28" height="28"> ScrapingBot: Universal API

ScrapingBot lets you scrape websites, generate text with ChatGPT, run Google searches, and query TikTok, Instagram, and Amazon data through the ScrapingBot API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scrapingBot/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 36
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://scraping-bot.io
- **Vendor API docs:** https://scraping-bot.io/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Google Search](actions/google-search.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/google-search?connectionId=$CONNECTION_ID&q=best%20web%20scraping%20tools%202025" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (36)

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Convert Amazon ASIN to GTIN](actions/convert-amazon-asin-to-gtin.md) | GET |  |
| [Generate ChatGPT Response](actions/generate-chat-gpt-response.md) | GET |  |
| [Get Amazon Product Details](actions/get-amazon-product-details.md) | GET |  |
| [Get Amazon Promo Code Details](actions/get-amazon-promo-code-details.md) | GET |  |
| [Get Amazon Seller Profile](actions/get-amazon-seller-profile.md) | GET |  |
| [Get Instagram Media by Shortcode](actions/get-instagram-media-by-shortcode.md) | GET |  |
| [Get Instagram Media by URL](actions/get-instagram-media-by-url.md) | GET |  |
| [Get Instagram User by ID](actions/get-instagram-user-by-id.md) | GET |  |
| [Get Instagram User by Username](actions/get-instagram-user-by-username.md) | GET |  |
| [Get TikTok Music Info](actions/get-tik-tok-music-info.md) | GET |  |
| [Get TikTok User Profile](actions/get-tik-tok-user-profile.md) | GET |  |
| [Get TikTok Video Information](actions/get-tik-tok-video-information.md) | GET |  |
| [Google Search](actions/google-search.md) | GET |  |
| [List Amazon Deal Products](actions/list-amazon-deal-products.md) | GET |  |
| [List Amazon Deals](actions/list-amazon-deals.md) | GET |  |
| [List Amazon Product Categories](actions/list-amazon-product-categories.md) | GET |  |
| [List Amazon Product Offers](actions/list-amazon-product-offers.md) | GET |  |
| [List Amazon Product Reviews](actions/list-amazon-product-reviews.md) | GET |  |
| [List Amazon Products by Category](actions/list-amazon-products-by-category.md) | GET |  |
| [List Amazon Seller Products](actions/list-amazon-seller-products.md) | GET |  |
| [List Amazon Seller Reviews](actions/list-amazon-seller-reviews.md) | GET |  |
| [List Amazon Top Product Reviews](actions/list-amazon-top-product-reviews.md) | GET |  |
| [List Instagram Media Comments](actions/list-instagram-media-comments.md) | GET |  |
| [List Instagram Tagged Posts](actions/list-instagram-tagged-posts.md) | GET |  |
| [List Instagram User Posts](actions/list-instagram-user-posts.md) | GET |  |
| [List Instagram User Reels](actions/list-instagram-user-reels.md) | GET |  |
| [List TikTok Music Posts](actions/list-tik-tok-music-posts.md) | GET |  |
| [List TikTok User Videos](actions/list-tik-tok-user-videos.md) | GET |  |
| [List TikTok Video Comments](actions/list-tik-tok-video-comments.md) | GET |  |
| [Scrape Website](actions/scrape-website.md) | GET |  |
| [Search Amazon Products](actions/search-amazon-products.md) | GET |  |
| [Search Instagram Hashtags](actions/search-instagram-hashtags.md) | GET |  |
| [Search Instagram Places](actions/search-instagram-places.md) | GET |  |
| [Search Instagram Users](actions/search-instagram-users.md) | GET |  |
| [Search TikTok Users](actions/search-tik-tok-users.md) | GET |  |
| [Search TikTok Videos](actions/search-tik-tok-videos.md) | GET |  |

