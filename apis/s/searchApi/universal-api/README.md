# <img src="https://images.mindcloud.co/apps/icons/search-api_1775755323603.png" alt="SearchApi logo" width="28" height="28"> SearchApi: Universal API

Search Google, maps, news, shopping, and other SearchApi results

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/searchApi/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.searchapi.io
- **Vendor API docs:** https://www.searchapi.io/docs/google

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/searchApi/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET |  |

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Reviews](actions/get-product-reviews.md) | GET |  |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Search Forums](actions/search-forums.md) | GET |  |

### Directions Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Directions](actions/get-directions.md) | GET |  |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Search Patents](actions/search-patents.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Search Videos](actions/search-videos.md) | GET |  |

### Image Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Images](actions/search-images.md) | GET |  |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Search Jobs](actions/search-jobs.md) | GET |  |

### Journeys

| Action | Method | Description |
| --- | --- | --- |
| [Search Flights](actions/search-flights.md) | GET |  |

### Keywords

| Action | Method | Description |
| --- | --- | --- |
| [Get Autocomplete Suggestions](actions/get-autocomplete-suggestions.md) | GET |  |
| [Search Trends](actions/search-trends.md) | GET |  |

### Knowledge Articles

| Action | Method | Description |
| --- | --- | --- |
| [Search Scholar](actions/search-scholar.md) | GET |  |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Search Hotels](actions/search-hotels.md) | GET |  |

### Map Photo

| Action | Method | Description |
| --- | --- | --- |
| [Get Map Photos](actions/get-map-photos.md) | GET |  |

### Map Place

| Action | Method | Description |
| --- | --- | --- |
| [Get Map Place](actions/get-map-place.md) | GET |  |

### Map Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Maps](actions/search-maps.md) | GET |  |

### Map Review

| Action | Method | Description |
| --- | --- | --- |
| [Get Map Reviews](actions/get-map-reviews.md) | GET |  |

### News Result

| Action | Method | Description |
| --- | --- | --- |
| [Search News](actions/search-news.md) | GET |  |

### Offers

| Action | Method | Description |
| --- | --- | --- |
| [Get Product Offers](actions/get-product-offers.md) | GET |  |

### Prices

| Action | Method | Description |
| --- | --- | --- |
| [Search Finance](actions/search-finance.md) | GET |  |

### Products

| Action | Method | Description |
| --- | --- | --- |
| [Get Product](actions/get-product.md) | GET |  |
| [Get Product Specs](actions/get-product-specs.md) | GET |  |

### Shopping Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Shopping](actions/search-shopping.md) | GET |  |

### Web Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Web](actions/search-web.md) | GET |  |

