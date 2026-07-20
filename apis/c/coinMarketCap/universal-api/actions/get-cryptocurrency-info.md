# CoinMarketCap: Get Cryptocurrency Info

Retrieves cryptocurrency metadata from CoinMarketCap.

```
GET https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-cryptocurrency-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CoinMarketCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-cryptocurrency-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coinMarketCap/latest/actions/get-cryptocurrency-info?${params}`, {
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
| `id` | string | no | CoinMarketCap cryptocurrency ID, for example 1. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "1": {
        "category": "string",
        "date_added": "2026-05-07T12:00:00.000Z",
        "date_launched": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "id": 1,
        "infinite_supply": true,
        "is_hidden": 1,
        "logo": "string",
        "name": "Ava Chen",
        "notice": "string",
        "slug": "string",
        "subreddit": "string",
        "symbol": "string",
        "tag-groups": [
          [
            "string"
          ]
        ],
        "tag-names": [
          [
            "Ava Chen"
          ]
        ],
        "tags": [
          [
            "string"
          ]
        ],
        "twitter_username": "Ava Chen",
        "urls": {
          "explorer": [
            [
              "https://example.com"
            ]
          ],
          "message_board": [
            [
              "https://example.com"
            ]
          ],
          "reddit": [
            [
              "https://example.com"
            ]
          ],
          "source_code": [
            [
              "https://example.com"
            ]
          ],
          "technical_doc": [
            [
              "https://example.com"
            ]
          ],
          "website": [
            [
              "https://example.com"
            ]
          ]
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `1.category` | string |  |
| `1.date_added` | date |  |
| `1.date_launched` | date |  |
| `1.description` | string |  |
| `1.id` | number |  |
| `1.infinite_supply` | boolean |  |
| `1.is_hidden` | number |  |
| `1.logo` | string |  |
| `1.name` | string |  |
| `1.notice` | string |  |
| `1.slug` | string |  |
| `1.subreddit` | string |  |
| `1.symbol` | string |  |
| `1.tag-groups[]` | array<string> |  |
| `1.tag-names[]` | array<string> |  |
| `1.tags[]` | array<string> |  |
| `1.twitter_username` | string |  |
| `1.urls.explorer[]` | array<string> |  |
| `1.urls.message_board[]` | array<string> |  |
| `1.urls.reddit[]` | array<string> |  |
| `1.urls.source_code[]` | array<string> |  |
| `1.urls.technical_doc[]` | array<string> |  |
| `1.urls.website[]` | array<string> |  |

## Native endpoint

Through the native CoinMarketCap API, this operation is `GET /v2/cryptocurrency/info` (base URL `https://pro-api.coinmarketcap.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-cryptocurrency-info.md) for the provider-specific parameters and requirements.

