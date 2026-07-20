# ScrapingBot: Native API Reference

A consolidated summary of ScrapingBot's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://scraping-bot.io/documentation
- **API base URL:** `https://scrapingbot.io/api/v1`

## Authentication

### ScrapingBot API Key

Use your ScrapingBot API key. Requests are authenticated with the x-api-key header.

### Credentials

- **API Key:** `apiKey` · optional · Your ScrapingBot API key.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://scraping-bot.io/documentation)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Convert Amazon ASIN to GTIN](actions/convert-amazon-asin-to-gtin.md) | `POST /amazon` | [docs](https://scraping-bot.io/documentation) |
| [Generate ChatGPT Response](actions/generate-chat-gpt-response.md) | `POST /chatgpt` | [docs](https://scraping-bot.io/documentation) |
| [Get Amazon Product Details](actions/get-amazon-product-details.md) | `POST /amazon` | [docs](https://scraping-bot.io/documentation) |
| [Get Amazon Promo Code Details](actions/get-amazon-promo-code-details.md) | `POST /amazon` | [docs](https://scraping-bot.io/documentation) |
| [Get Amazon Seller Profile](actions/get-amazon-seller-profile.md) | `POST /amazon` | [docs](https://scraping-bot.io/documentation) |
| [Get Instagram Media by Shortcode](actions/get-instagram-media-by-shortcode.md) | `POST /instagram` | [docs](https://scraping-bot.io/documentation) |
| [Get Instagram Media by URL](actions/get-instagram-media-by-url.md) | `POST /instagram` | [docs](https://scraping-bot.io/documentation) |
| [Get Instagram User by ID](actions/get-instagram-user-by-id.md) | `POST /instagram` | [docs](https://scraping-bot.io/documentation) |
| [Get Instagram User by Username](actions/get-instagram-user-by-username.md) | `POST /instagram` | [docs](https://scraping-bot.io/documentation) |
| [Get TikTok Music Info](actions/get-tik-tok-music-info.md) | `POST /tiktok` | [docs](https://scraping-bot.io/documentation) |
| [Get TikTok User Profile](actions/get-tik-tok-user-profile.md) | `POST /tiktok` | [docs](https://scraping-bot.io/documentation) |
| [Get TikTok Video Information](actions/get-tik-tok-video-information.md) | `POST /tiktok` | [docs](https://scraping-bot.io/documentation) |
| [Google Search](actions/google-search.md) | `POST /google` | [docs](https://scraping-bot.io/documentation) |
| [List Amazon Deal Products](actions/list-amazon-deal-products.md) | `POST /amazon` | [docs](https://scraping-bot.io/documentation) |
| [List Amazon Deals](actions/list-amazon-deals.md) | `POST /amazon` | [docs](https://scraping-bot.io/documentation) |
| [List Amazon Product Categories](actions/list-amazon-product-categories.md) | `POST /amazon` | [docs](https://scraping-bot.io/documentation) |
| [List Amazon Product Offers](actions/list-amazon-product-offers.md) | `POST /amazon` | [docs](https://scraping-bot.io/documentation) |
| [List Amazon Product Reviews](actions/list-amazon-product-reviews.md) | `POST /amazon` | [docs](https://scraping-bot.io/documentation) |
| [List Amazon Products by Category](actions/list-amazon-products-by-category.md) | `POST /amazon` | [docs](https://scraping-bot.io/documentation) |
| [List Amazon Seller Products](actions/list-amazon-seller-products.md) | `POST /amazon` | [docs](https://scraping-bot.io/documentation) |
| [List Amazon Seller Reviews](actions/list-amazon-seller-reviews.md) | `POST /amazon` | [docs](https://scraping-bot.io/documentation) |
| [List Amazon Top Product Reviews](actions/list-amazon-top-product-reviews.md) | `POST /amazon` | [docs](https://scraping-bot.io/documentation) |
| [List Instagram Media Comments](actions/list-instagram-media-comments.md) | `POST /instagram` | [docs](https://scraping-bot.io/documentation) |
| [List Instagram Tagged Posts](actions/list-instagram-tagged-posts.md) | `POST /instagram` | [docs](https://scraping-bot.io/documentation) |
| [List Instagram User Posts](actions/list-instagram-user-posts.md) | `POST /instagram` | [docs](https://scraping-bot.io/documentation) |
| [List Instagram User Reels](actions/list-instagram-user-reels.md) | `POST /instagram` | [docs](https://scraping-bot.io/documentation) |
| [List TikTok Music Posts](actions/list-tik-tok-music-posts.md) | `POST /tiktok` | [docs](https://scraping-bot.io/documentation) |
| [List TikTok User Videos](actions/list-tik-tok-user-videos.md) | `POST /tiktok` | [docs](https://scraping-bot.io/documentation) |
| [List TikTok Video Comments](actions/list-tik-tok-video-comments.md) | `POST /tiktok` | [docs](https://scraping-bot.io/documentation) |
| [Scrape Website](actions/scrape-website.md) | `GET /scrape` | [docs](https://scraping-bot.io/documentation) |
| [Search Amazon Products](actions/search-amazon-products.md) | `POST /amazon` | [docs](https://scraping-bot.io/documentation) |
| [Search Instagram Hashtags](actions/search-instagram-hashtags.md) | `POST /instagram` | [docs](https://scraping-bot.io/documentation) |
| [Search Instagram Places](actions/search-instagram-places.md) | `POST /instagram` | [docs](https://scraping-bot.io/documentation) |
| [Search Instagram Users](actions/search-instagram-users.md) | `POST /instagram` | [docs](https://scraping-bot.io/documentation) |
| [Search TikTok Users](actions/search-tik-tok-users.md) | `POST /tiktok` | [docs](https://scraping-bot.io/documentation) |
| [Search TikTok Videos](actions/search-tik-tok-videos.md) | `POST /tiktok` | [docs](https://scraping-bot.io/documentation) |
