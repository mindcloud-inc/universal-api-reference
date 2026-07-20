# Adyntel: Search LinkedIn Ads by Keyword

Finds LinkedIn ads in Adyntel by keyword.

```
GET https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/search-linked-in-ads-by-keyword
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Adyntel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/search-linked-in-ads-by-keyword?connectionId=$CONNECTION_ID&keyword=shopify" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyword": "shopify"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/search-linked-in-ads-by-keyword?${params}`, {
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
| `keyword` | string | yes | Keyword to search in the LinkedIn Ad Library. Example: `shopify`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ads": [
        {}
      ],
      "continuation_token": "string",
      "has_more": true,
      "total_ads": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ads` | array<object> |  |
| `continuation_token` | string |  |
| `has_more` | boolean |  |
| `total_ads` | number |  |

## Native endpoint

Through the native Adyntel API, this operation is `POST /linkedin-keyword-search` (base URL `https://api.adyntel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-linked-in-ads-by-keyword.md) for the provider-specific parameters and requirements.

