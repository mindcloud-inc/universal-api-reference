# Pipeless Recommendations: Get Relationship Counts

Retrieves relationship counts for an object in Pipeless Recommendations.

```
GET https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-relationship-counts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipeless Recommendations `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-relationship-counts?connectionId=$CONNECTION_ID&appId=1885" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appId": "1885"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipelessRecommendations/latest/actions/get-relationship-counts?${params}`, {
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
| `appId` | string | yes | Numeric Pipeless app ID. Default: `1885`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number | Relationship count result. |

## Native endpoint

Through the native Pipeless Recommendations API, this operation is `GET /v1/apps/:appId/relationship-counts` (base URL `https://api.pipeless.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-relationship-counts.md) for the provider-specific parameters and requirements.

