# ScrapingBot: Search Instagram Places



```
GET https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/search-instagram-places
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/search-instagram-places?connectionId=$CONNECTION_ID&keyword=new%20york" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyword": "new york"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/search-instagram-places?${params}`, {
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
| `keyword` | string | yes | Keyword to search for places. Default: `new york`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsUsed": 1,
      "duration": "string",
      "query": "string",
      "results": [
        {}
      ],
      "status": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsUsed` | number |  |
| `duration` | string |  |
| `query` | string |  |
| `results` | array<object> |  |
| `status` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native ScrapingBot API, this operation is `POST /instagram` (base URL `https://scrapingbot.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-instagram-places.md) for the provider-specific parameters and requirements.

