# Rollbar: Get Occurrence Metrics

Retrieves occurrence metrics from Rollbar.

```
GET https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/get-occurrence-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rollbar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/get-occurrence-metrics?connectionId=$CONNECTION_ID&endTime=1&startTime=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "endTime": "1",
  "startTime": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/get-occurrence-metrics?${params}`, {
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
| `endTime` | number | yes | Unix timestamp of the query end time |
| `startTime` | number | yes | Unix timestamp of the query start time |

## Response

```json
{
  "success": true,
  "data": [
    {
      "err": 1,
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `err` | number |  |
| `result` | object |  |

## Native endpoint

Through the native Rollbar API, this operation is `POST /metrics/occurrences` (base URL `https://api.rollbar.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-occurrence-metrics.md) for the provider-specific parameters and requirements.

