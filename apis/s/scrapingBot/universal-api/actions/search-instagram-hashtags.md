# ScrapingBot: Search Instagram Hashtags



```
GET https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/search-instagram-hashtags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScrapingBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/search-instagram-hashtags?connectionId=$CONNECTION_ID&keyword=instagram" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "keyword": "instagram"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapingBot/latest/actions/search-instagram-hashtags?${params}`, {
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
| `keyword` | string | yes | Keyword to search for hashtags. Default: `instagram`. |

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

Through the native ScrapingBot API, this operation is `POST /instagram` (base URL `https://scrapingbot.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-instagram-hashtags.md) for the provider-specific parameters and requirements.

