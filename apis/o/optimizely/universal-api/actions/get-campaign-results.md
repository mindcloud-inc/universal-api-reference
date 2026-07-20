# Optimizely: Get Campaign Results

Retrieves results for a campaign in Optimizely.

```
GET https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-campaign-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Optimizely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-campaign-results?connectionId=$CONNECTION_ID&campaignId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/optimizely/latest/actions/get-campaign-results?${params}`, {
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
| `campaignId` | string | yes | The campaign id to fetch results for. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": 1,
      "confidenceThreshold": 1,
      "endTime": "string",
      "isStale": true,
      "metrics": [
        {}
      ],
      "startTime": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | number |  |
| `confidenceThreshold` | number |  |
| `endTime` | string |  |
| `isStale` | boolean |  |
| `metrics` | array<object> |  |
| `startTime` | string |  |

## Native endpoint

Through the native Optimizely API, this operation is `GET /campaigns/{campaignId}/results` (base URL `https://api.optimizely.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-results.md) for the provider-specific parameters and requirements.

