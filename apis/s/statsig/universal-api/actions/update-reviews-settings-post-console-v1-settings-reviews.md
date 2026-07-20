# Statsig: Update Reviews Settings

Updates review settings in Statsig.

```
PUT https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-reviews-settings-post-console-v1-settings-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-reviews-settings-post-console-v1-settings-reviews" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "isConfigReviewRequired": true,
  "isMetricReviewRequired": true,
  "isMetricReviewRequiredOnVerifiedOnly": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-reviews-settings-post-console-v1-settings-reviews', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "isConfigReviewRequired": true,
    "isMetricReviewRequired": true,
    "isMetricReviewRequiredOnVerifiedOnly": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isConfigReviewRequired` | boolean | yes | Request body field. |
| `isMetricReviewRequired` | boolean | yes | Request body field. |
| `isMetricReviewRequiredOnVerifiedOnly` | boolean | yes | Request body field. |
| `isWhnAnalysisOnlyReviewRequired` | boolean | no | Request body field. |
| `isWhnSourceReviewRequired` | boolean | no | Request body field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `POST /console/v1/settings/reviews` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-reviews-settings-post-console-v1-settings-reviews.md) for the provider-specific parameters and requirements.

