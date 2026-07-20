# InsightIQ: Create Async Creator Profile Analytics

Creates an async creator analytics request in InsightIQ.

```
POST https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/create-async-creator-profile-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InsightIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/create-async-creator-profile-analytics" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "identifier": "string",
  "workPlatformId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/create-async-creator-profile-analytics', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "identifier": "string",
    "workPlatformId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `identifier` | string | yes | URL, username, handle, or profile URL to analyze |
| `isPremium` | boolean | no | Premium analytics mode for Twitch only |
| `metricCalculationMethod` | string | no | Metric aggregation method; supports average or median Default: `average`. |
| `workPlatformId` | string | yes | Work platform ID for the profile lookup |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "identifier": "string",
      "status": "string",
      "work_platform": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `identifier` | string |  |
| `status` | string |  |
| `work_platform` | object |  |

## Native endpoint

Through the native InsightIQ API, this operation is `POST /v1/social/creators/async/profiles/analytics` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-async-creator-profile-analytics.md) for the provider-specific parameters and requirements.

