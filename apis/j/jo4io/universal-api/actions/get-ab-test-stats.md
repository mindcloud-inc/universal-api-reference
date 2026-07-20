# jo4.io: Get A/B Test Stats



```
GET https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-ab-test-stats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a jo4.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-ab-test-stats?connectionId=$CONNECTION_ID&slug=de80effb9e48402a83afc77f947f82e4" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "de80effb9e48402a83afc77f947f82e4"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jo4io/latest/actions/get-ab-test-stats?${params}`, {
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
| `slug` | string | yes | Default: `de80effb9e48402a83afc77f947f82e4`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bestVariantId": 1,
      "bestVariantName": "Ava Chen",
      "endedAt": 1,
      "hasStatisticalSignificance": true,
      "minVisitorsRequired": 1,
      "slug": "string",
      "startedAt": 1,
      "status": "string",
      "totalConversions": 1,
      "totalRevenue": 1,
      "totalVisitors": 1,
      "urlId": 1,
      "variants": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bestVariantId` | number |  |
| `bestVariantName` | string |  |
| `endedAt` | number |  |
| `hasStatisticalSignificance` | boolean |  |
| `minVisitorsRequired` | number |  |
| `slug` | string |  |
| `startedAt` | number |  |
| `status` | string |  |
| `totalConversions` | number |  |
| `totalRevenue` | number |  |
| `totalVisitors` | number |  |
| `urlId` | number |  |
| `variants` | array<object> |  |

## Native endpoint

Through the native jo4.io API, this operation is `GET /protected/url/:slug/ab-test` (base URL `https://jo4-api.jo4.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ab-test-stats.md) for the provider-specific parameters and requirements.

