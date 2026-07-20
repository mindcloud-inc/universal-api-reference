# Robopost: Get Aggregated Analytics by ID

Retrieves aggregated analytics from Robopost by ID.

```
GET https://connect.mindcloud.co/v1/universal/robopost/latest/actions/get-aggregated-analytics-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Robopost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/robopost/latest/actions/get-aggregated-analytics-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/robopost/latest/actions/get-aggregated-analytics-by-id?${params}`, {
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
| `id` | string | yes | The aggregated analytics record ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "analyticsLastSync": "2026-05-07T12:00:00.000Z",
      "commentsCount": 1,
      "dt": "2026-05-07T12:00:00.000Z",
      "engagementRate": 1,
      "engagementsTotal": 1,
      "impressions": 1,
      "interval": "string",
      "reactionsLike": 1,
      "savesCount": 1,
      "sharesCount": 1,
      "socialNetwork": "string",
      "teamId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `analyticsLastSync` | date | Last analytics sync time. |
| `commentsCount` | number | Comments count. |
| `dt` | date | Analytics bucket datetime. |
| `engagementRate` | number | Engagement rate. |
| `engagementsTotal` | number | Total engagements. |
| `impressions` | number | Total impressions. |
| `interval` | string | Analytics interval. |
| `reactionsLike` | number | Like reactions count. |
| `savesCount` | number | Saves count. |
| `sharesCount` | number | Shares count. |
| `socialNetwork` | string | Social network for the analytics row. |
| `teamId` | string | Robopost team ID. |

## Native endpoint

Through the native Robopost API, this operation is `GET /aggregated_posts_analytics/{id}` (base URL `https://public-api.robopost.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-aggregated-analytics-by-id.md) for the provider-specific parameters and requirements.

