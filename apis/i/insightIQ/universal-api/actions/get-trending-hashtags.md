# InsightIQ: Get Trending Hashtags

Retrieves current trending hashtags from InsightIQ.

```
GET https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-trending-hashtags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InsightIQ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-trending-hashtags?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-trending-hashtags?${params}`, {
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
| `countryCode` | string | no | ISO 2-letter country code Default: `US`. |
| `industry` | string | no | Industry to get popular hashtags from |
| `period` | number | no | Time window in days for trend calculation Default: `7`. |
| `workPlatformId` | string | no | Work platform ID for the TikTok trends source |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "metadata": {},
      "work_platform": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `metadata` | object |  |
| `work_platform` | object |  |

## Native endpoint

Through the native InsightIQ API, this operation is `GET /v1/trends/hashtag` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-trending-hashtags.md) for the provider-specific parameters and requirements.

