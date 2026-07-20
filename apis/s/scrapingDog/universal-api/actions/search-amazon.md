# ScrapingDog: Search Amazon

Retrieves Amazon search results through ScrapingDog.

```
GET https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-amazon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingDog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-amazon?connectionId=$CONNECTION_ID&domain=string&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string",
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingDog/latest/actions/search-amazon?${params}`, {
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
| `country` | string | no | Target Amazon country code. Default: `us`. |
| `domain` | string | yes | Amazon top-level domain. |
| `page` | string | no | Amazon search results page. |
| `query` | string | yes | Amazon search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        [
          [
            "string"
          ]
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[]` | array<array> |  |

## Native endpoint

Through the native ScrapingDog API, this operation is `GET /amazon/search` (base URL `https://api.scrapingdog.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-amazon.md) for the provider-specific parameters and requirements.

