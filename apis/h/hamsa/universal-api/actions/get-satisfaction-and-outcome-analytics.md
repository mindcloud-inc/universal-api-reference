# Hamsa: Get Satisfaction and Outcome Analytics

Retrieves voice agent satisfaction and outcome analytics from Hamsa.

```
GET https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-satisfaction-and-outcome-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hamsa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-satisfaction-and-outcome-analytics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hamsa/latest/actions/get-satisfaction-and-outcome-analytics?${params}`, {
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
| `endPeriod` | string | no |  |
| `period` | string | no | Default: `TODAY`. |
| `startPeriod` | string | no |  |
| `timeDifference` | string | no | Default: `0`. |
| `voiceAgentId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "csatScore": 1,
      "escalationRate": 1,
      "firstCallResolutionPercentage": 1,
      "npsScore": 1,
      "sentimentDistribution": {
        "negative": 1,
        "neutral": 1,
        "positive": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `csatScore` | number |  |
| `escalationRate` | number |  |
| `firstCallResolutionPercentage` | number |  |
| `npsScore` | number |  |
| `sentimentDistribution.negative` | number |  |
| `sentimentDistribution.neutral` | number |  |
| `sentimentDistribution.positive` | number |  |

## Native endpoint

Through the native Hamsa API, this operation is `GET /v1/agent-analytics/satisfaction` (base URL `https://api.tryhamsa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-satisfaction-and-outcome-analytics.md) for the provider-specific parameters and requirements.

