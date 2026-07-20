# Rollbar: Get Resolution Time Metrics

Retrieves resolution time metrics from Rollbar.

```
GET https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/get-resolution-time-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rollbar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/get-resolution-time-metrics?connectionId=$CONNECTION_ID&projectIds=string&startTime=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectIds": "string",
  "startTime": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rollbar/latest/actions/get-resolution-time-metrics?${params}`, {
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
| `projectIds` | string | yes | List of Rollbar project IDs |
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

Through the native Rollbar API, this operation is `POST /metrics/ttr` (base URL `https://api.rollbar.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-resolution-time-metrics.md) for the provider-specific parameters and requirements.

