# wttr.in: Get Weather Metrics

Retrieves Prometheus weather metrics from wttr.in.

```
GET https://connect.mindcloud.co/v1/universal/wttrin/latest/actions/get-weather-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a wttr.in `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wttrin/latest/actions/get-weather-metrics?connectionId=$CONNECTION_ID&location=London" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "location": "London"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wttrin/latest/actions/get-weather-metrics?${params}`, {
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
| `location` | string | yes | City, airport code, domain, postal code, GPS coordinates, or supported wttr.in location expression. Example: `London`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | UTF-8 byte values for the Prometheus metrics payload. |
| `type` | string | Runtime buffer marker for the raw Prometheus text response. |

## Native endpoint

Through the native wttr.in API, this operation is `GET /[:location]` (base URL `https://wttr.in`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-weather-metrics.md) for the provider-specific parameters and requirements.

