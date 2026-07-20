# Adyntel: Search Meta Ads by Keyword

Finds Meta ads in Adyntel by keyword.

```
GET https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/search-meta-ads-by-keyword
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adyntel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/search-meta-ads-by-keyword?connectionId=$CONNECTION_ID&keyword=shopify" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyword": "shopify"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/search-meta-ads-by-keyword?${params}`, {
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
| `keyword` | string | yes | Keyword to search in the Meta Ad Library. Default: `shopify`. Example: `shopify`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active_status": "string",
      "ad_type": "string",
      "continuation_token": "string",
      "country_code": "string",
      "is_result_complete": true,
      "media_types": "string",
      "number_of_ads": 1,
      "platform": "string",
      "query": "string",
      "results": [
        {}
      ],
      "search_type": "string",
      "start_max_date": "string",
      "start_min_date": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active_status` | string |  |
| `ad_type` | string |  |
| `continuation_token` | string |  |
| `country_code` | string |  |
| `is_result_complete` | boolean |  |
| `media_types` | string |  |
| `number_of_ads` | number |  |
| `platform` | string |  |
| `query` | string |  |
| `results` | array<object> |  |
| `search_type` | string |  |
| `start_max_date` | string |  |
| `start_min_date` | string |  |

## Native endpoint

Through the native Adyntel API, this operation is `POST /facebook_ad_search` (base URL `https://api.adyntel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-meta-ads-by-keyword.md) for the provider-specific parameters and requirements.

