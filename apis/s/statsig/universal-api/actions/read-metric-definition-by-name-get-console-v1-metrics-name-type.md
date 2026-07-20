# Statsig: Read Metric Definition by Name

Retrieves a metric definition by name from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/read-metric-definition-by-name-get-console-v1-metrics-name-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/read-metric-definition-by-name-get-console-v1-metrics-name-type?connectionId=$CONNECTION_ID&name=Ava%20Chen&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/read-metric-definition-by-name-get-console-v1-metrics-name-type?${params}`, {
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
| `name` | string | yes | name |
| `type` | string | yes | type |

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

Through the native Statsig API, this operation is `GET /console/v1/metrics/{name}/{type}` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-metric-definition-by-name-get-console-v1-metrics-name-type.md) for the provider-specific parameters and requirements.

