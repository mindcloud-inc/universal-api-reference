# Postpone: Get Post Time Series Metrics

Retrieves post time series metrics from Postpone.

```
GET https://connect.mindcloud.co/v1/universal/postpone/latest/actions/get-post-time-series-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postpone `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postpone/latest/actions/get-post-time-series-metrics?connectionId=$CONNECTION_ID&variables.startDate=string&variables.endDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "variables.startDate": "string",
  "variables.endDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postpone/latest/actions/get-post-time-series-metrics?${params}`, {
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
| `variables.startDate` | string | yes |  |
| `variables.endDate` | string | yes |  |
| `variables.socialAccountIds[]` | array<string> | no |  |
| `variables.metrics[]` | array<string> | no |  |
| `variables.groupBy` | string | no |  |
| `variables.subreddits[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "isoWeek": 1,
      "isoYear": 1,
      "metrics": [
        {
          "metric": "string",
          "value": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date |  |
| `isoWeek` | number |  |
| `isoYear` | number |  |
| `metrics[].metric` | string |  |
| `metrics[].value` | number |  |

## Native endpoint

Through the native Postpone API, this operation is `POST /gql` (base URL `https://api.postpone.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post-time-series-metrics.md) for the provider-specific parameters and requirements.

