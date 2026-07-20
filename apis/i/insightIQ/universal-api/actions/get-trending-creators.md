# InsightIQ: Get Trending Creators

Retrieves current trending creators from InsightIQ.

```
GET https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-trending-creators
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InsightIQ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-trending-creators?connectionId=$CONNECTION_ID&limit=25&offset=0&workPlatformId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workPlatformId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/get-trending-creators?${params}`, {
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
| `audienceCountry` | string | no | Audience country code |
| `creatorCountry` | string | no | Creator country code |
| `followerCount` | string | no | Filter creators by follower count range |
| `sortBy` | string | no | Sort creators by engagement, follower, or avg_views |
| `workPlatformId` | string | yes | Work platform ID for the platform on which you want to get the trending TikTok creator data. |

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

Through the native InsightIQ API, this operation is `GET /v1/trends/creators` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-trending-creators.md) for the provider-specific parameters and requirements.

