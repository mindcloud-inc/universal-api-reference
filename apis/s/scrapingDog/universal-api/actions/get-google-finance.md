# ScrapingDog: Get Google Finance

Retrieves Google Finance data through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-finance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-finance?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/get-google-finance?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | Ticker or finance query to search on Google Finance. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "discover_more": {
        "items": {
          "link": "https://example.com",
          "name": "Ava Chen",
          "price": 1,
          "price_movement": {
            "movement": "string",
            "percentage": 1
          },
          "scrapingdog_link": "https://example.com",
          "stock": "string"
        },
        "title": "string"
      },
      "knowledge_graph": {
        "about": [
          "string"
        ],
        "key_stats": {
          "stats": {
            "label": "string",
            "value": "string"
          },
          "tags": {
            "link": "https://example.com",
            "title": "string"
          }
        }
      },
      "market": {
        "Asia": {
          "link": "https://example.com",
          "name": "Ava Chen",
          "price": "string",
          "price_movement": {
            "movement": "string",
            "percentage": "string",
            "value": "string"
          },
          "scrapingdog_link": "https://example.com",
          "stock": "string"
        },
        "Crypto": {
          "link": "https://example.com",
          "name": "Ava Chen",
          "price": "string",
          "price_movement": {
            "movement": "string",
            "percentage": "string",
            "value": "string"
          },
          "scrapingdog_link": "https://example.com",
          "stock": "string"
        },
        "Currencies": {
          "link": "https://example.com",
          "name": "Ava Chen",
          "price": "string",
          "price_movement": {
            "movement": "string",
            "percentage": "string",
            "value": "string"
          },
          "scrapingdog_link": "https://example.com",
          "stock": "string"
        },
        "Europe": {
          "link": "https://example.com",
          "name": "Ava Chen",
          "price": "string",
          "price_movement": {
            "movement": "string",
            "percentage": "string",
            "value": "string"
          },
          "scrapingdog_link": "https://example.com",
          "stock": "string"
        },
        "Futures": {
          "link": "https://example.com",
          "name": "Ava Chen",
          "price": "string",
          "price_movement": {
            "movement": "string",
            "percentage": "string",
            "value": "string"
          },
          "scrapingdog_link": "https://example.com",
          "stock": "string"
        },
        "US": {
          "link": "https://example.com",
          "name": "Ava Chen",
          "price": "string",
          "price_movement": {
            "movement": "string",
            "percentage": "string",
            "value": "string"
          },
          "scrapingdog_link": "https://example.com",
          "stock": "string"
        }
      },
      "market_news": {
        "link": "https://example.com",
        "snippet": "string",
        "source": "string",
        "time": "string"
      },
      "summary": {
        "exchange": "string",
        "extracted_price": 1,
        "price": "string",
        "price_movement": {
          "movement": "string",
          "percentage": 1,
          "value": 1
        },
        "stock": "string",
        "time": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `discover_more` | array<object> |  |
| `discover_more.items` | array<object> |  |
| `discover_more.items.link` | string |  |
| `discover_more.items.name` | string |  |
| `discover_more.items.price` | number |  |
| `discover_more.items.price_movement` | object |  |
| `discover_more.items.price_movement.movement` | string |  |
| `discover_more.items.price_movement.percentage` | number |  |
| `discover_more.items.scrapingdog_link` | string |  |
| `discover_more.items.stock` | string |  |
| `discover_more.title` | string |  |
| `knowledge_graph` | object |  |
| `knowledge_graph.about` | array<string> |  |
| `knowledge_graph.key_stats` | object |  |
| `knowledge_graph.key_stats.stats` | array<object> |  |
| `knowledge_graph.key_stats.stats.label` | string |  |
| `knowledge_graph.key_stats.stats.value` | string |  |
| `knowledge_graph.key_stats.tags` | array<object> |  |
| `knowledge_graph.key_stats.tags.link` | string |  |
| `knowledge_graph.key_stats.tags.title` | string |  |
| `market` | object |  |
| `market_news` | array<object> |  |
| `market_news.link` | string |  |
| `market_news.snippet` | string |  |
| `market_news.source` | string |  |
| `market_news.time` | string |  |
| `market.Asia` | array<object> |  |
| `market.Asia.link` | string |  |
| `market.Asia.name` | string |  |
| `market.Asia.price` | string |  |
| `market.Asia.price_movement` | object |  |
| `market.Asia.price_movement.movement` | string |  |
| `market.Asia.price_movement.percentage` | string |  |
| `market.Asia.price_movement.value` | string |  |
| `market.Asia.scrapingdog_link` | string |  |
| `market.Asia.stock` | string |  |
| `market.Crypto` | array<object> |  |
| `market.Crypto.link` | string |  |
| `market.Crypto.name` | string |  |
| `market.Crypto.price` | string |  |
| `market.Crypto.price_movement` | object |  |
| `market.Crypto.price_movement.movement` | string |  |
| `market.Crypto.price_movement.percentage` | string |  |
| `market.Crypto.price_movement.value` | string |  |
| `market.Crypto.scrapingdog_link` | string |  |
| `market.Crypto.stock` | string |  |
| `market.Currencies` | array<object> |  |
| `market.Currencies.link` | string |  |
| `market.Currencies.name` | string |  |
| `market.Currencies.price` | string |  |
| `market.Currencies.price_movement` | object |  |
| `market.Currencies.price_movement.movement` | string |  |
| `market.Currencies.price_movement.percentage` | string |  |
| `market.Currencies.price_movement.value` | string |  |
| `market.Currencies.scrapingdog_link` | string |  |
| `market.Currencies.stock` | string |  |
| `market.Europe` | array<object> |  |
| `market.Europe.link` | string |  |
| `market.Europe.name` | string |  |
| `market.Europe.price` | string |  |
| `market.Europe.price_movement` | object |  |
| `market.Europe.price_movement.movement` | string |  |
| `market.Europe.price_movement.percentage` | string |  |
| `market.Europe.price_movement.value` | string |  |
| `market.Europe.scrapingdog_link` | string |  |
| `market.Europe.stock` | string |  |
| `market.Futures` | array<object> |  |
| `market.Futures.link` | string |  |
| `market.Futures.name` | string |  |
| `market.Futures.price` | string |  |
| `market.Futures.price_movement` | object |  |
| `market.Futures.price_movement.movement` | string |  |
| `market.Futures.price_movement.percentage` | string |  |
| `market.Futures.price_movement.value` | string |  |
| `market.Futures.scrapingdog_link` | string |  |
| `market.Futures.stock` | string |  |
| `market.US` | array<object> |  |
| `market.US.link` | string |  |
| `market.US.name` | string |  |
| `market.US.price` | string |  |
| `market.US.price_movement` | object |  |
| `market.US.price_movement.movement` | string |  |
| `market.US.price_movement.percentage` | string |  |
| `market.US.price_movement.value` | string |  |
| `market.US.scrapingdog_link` | string |  |
| `market.US.stock` | string |  |
| `summary` | object |  |
| `summary.exchange` | string |  |
| `summary.extracted_price` | number |  |
| `summary.price` | string |  |
| `summary.price_movement` | object |  |
| `summary.price_movement.movement` | string |  |
| `summary.price_movement.percentage` | number |  |
| `summary.price_movement.value` | number |  |
| `summary.stock` | string |  |
| `summary.time` | string |  |
| `summary.title` | string |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /google_finance` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-google-finance.md) for the provider-specific parameters and requirements.

