# Retently: Get Latest Score

Retrieves the latest metric score from Retently.

```
GET https://connect.mindcloud.co/v1/universal/retently/latest/actions/get-latest-score
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retently/latest/actions/get-latest-score?connectionId=$CONNECTION_ID&metric=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "metric": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retently/latest/actions/get-latest-score?${params}`, {
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
| `metric` | string | yes | Metric key such as nps, csat, or ces. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "detractors": 1,
      "detractorsCount": 1,
      "metricsType": "string",
      "passives": 1,
      "passivesCount": 1,
      "promoters": 1,
      "promotersCount": 1,
      "score": 1,
      "scoreSum": 1,
      "totalResponses": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `detractors` | number |  |
| `detractorsCount` | number |  |
| `metricsType` | string |  |
| `passives` | number |  |
| `passivesCount` | number |  |
| `promoters` | number |  |
| `promotersCount` | number |  |
| `score` | number |  |
| `scoreSum` | number |  |
| `totalResponses` | number |  |

## Native endpoint

Through the native Retently API, this operation is `GET /api/v2/:metric/score` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-latest-score.md) for the provider-specific parameters and requirements.

