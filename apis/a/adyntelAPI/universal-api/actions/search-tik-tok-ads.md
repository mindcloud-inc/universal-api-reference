# Adyntel: Search TikTok Ads

Finds TikTok ads in Adyntel by keyword.

```
GET https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/search-tik-tok-ads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adyntel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/search-tik-tok-ads?connectionId=$CONNECTION_ID&keyword=shopify" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyword": "shopify"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/search-tik-tok-ads?${params}`, {
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
| `keyword` | string | yes | Search query for the TikTok ad library. Example: `shopify`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": [
        {}
      ],
      "has_more": true,
      "search_id": "string",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | array<object> |  |
| `has_more` | boolean |  |
| `search_id` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Adyntel API, this operation is `POST /tiktok_search` (base URL `https://api.adyntel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-tik-tok-ads.md) for the provider-specific parameters and requirements.

