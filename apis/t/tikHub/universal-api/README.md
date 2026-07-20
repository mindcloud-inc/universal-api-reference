# <img src="https://images.mindcloud.co/apps/icons/tik-hub_1774389937741.png" alt="TikHub logo" width="28" height="28"> TikHub: Universal API

Search social content, profiles, products, and analytics across major platforms

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tikHub/latest
- **Category:** Marketing / Social Media
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.tikhub.io
- **Vendor API docs:** https://docs.tikhub.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get TikHub User Info](actions/get-tik-hub-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikHub/latest/actions/get-tik-hub-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Endpoint Price

| Action | Method | Description |
| --- | --- | --- |
| [Calculate Endpoint Price](actions/calculate-endpoint-price.md) | GET | Calculates API endpoint pricing in TikHub. |

### Product Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Categories](actions/get-product-categories.md) | GET | Retrieves TikTok Shop product categories from TikHub. |

### Product Search Keyword

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Search Suggestions](actions/get-product-search-suggestions.md) | GET | Finds TikTok Shop product search suggestions in TikHub. |

### Search Keyword

| Action | Method | Description |
| --- | --- | --- |
| [Get Search Keyword Suggestions](actions/get-search-keyword-suggestions.md) | GET | Finds TikTok search keyword suggestions in TikHub. |
| [Get Trending Search Keywords](actions/get-trending-search-keywords.md) | GET | Retrieves trending TikTok search keywords from TikHub. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Get General Search Results](actions/get-general-search-results.md) | GET | Retrieves general TikTok search results from TikHub. |

### Tiered Discount

| Action | Method | Description |
| --- | --- | --- |
| [Get Tiered Discount Info](actions/get-tiered-discount-info.md) | GET | Retrieves tiered discount information from TikHub. |

### Tikhub Endpoint

| Action | Method | Description |
| --- | --- | --- |
| [Get All Endpoints Info](actions/get-all-endpoints-info.md) | GET | Retrieves details for all TikHub endpoints. |
| [Get Endpoint Info](actions/get-endpoint-info.md) | GET | Retrieves details for a TikHub endpoint. |

### Tikhub User

| Action | Method | Description |
| --- | --- | --- |
| [Get TikHub User Info](actions/get-tik-hub-user-info.md) | GET | Retrieves the current TikHub user info. |
| [Get User Daily Usage](actions/get-user-daily-usage.md) | GET | Retrieves daily API usage from TikHub. |

### Tiktok Comment

| Action | Method | Description |
| --- | --- | --- |
| [Get Video Comments](actions/get-video-comments.md) | GET | Retrieves comments for a TikTok video from TikHub. |

### Tiktok Shop Product

| Action | Method | Description |
| --- | --- | --- |
| [Get Hot Selling Products](actions/get-hot-selling-products.md) | GET | Retrieves hot-selling TikTok Shop products from TikHub. |
| [Get Product Detail](actions/get-product-detail.md) | GET | Retrieves TikTok Shop product details from TikHub. |
| [Get Seller Products](actions/get-seller-products.md) | GET | Retrieves TikTok Shop products for a seller from TikHub. |
| [Search Products](actions/search-products.md) | GET | Finds TikTok Shop products in TikHub by keyword. |

### Tiktok User

| Action | Method | Description |
| --- | --- | --- |
| [Get User IDs by Username](actions/get-user-ids-by-username.md) | GET | Retrieves TikTok user IDs from TikHub by username. |
| [Get User Profile](actions/get-user-profile.md) | GET | Retrieves a TikTok user profile from TikHub. |
| [Get User Profile by Identifier](actions/get-user-profile-by-identifier.md) | GET | Retrieves a TikTok user profile from TikHub by identifier. |

### Tiktok Video

| Action | Method | Description |
| --- | --- | --- |
| [Get Single Video](actions/get-single-video.md) | GET | Retrieves a TikTok video from TikHub. |
| [Get User Posts](actions/get-user-posts.md) | GET | Retrieves TikTok posts for a user from TikHub. |
| [Get Video Detail](actions/get-video-detail.md) | GET | Retrieves TikTok video details from TikHub. |
| [Get Video Search Results](actions/get-video-search-results.md) | GET | Retrieves TikTok video search results from TikHub. |
| [Search Videos](actions/search-videos.md) | GET | Finds TikTok videos in TikHub by keyword. |

