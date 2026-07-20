# Grafana: Export Mute Timings

Exports mute timings from Grafana.

```
GET https://connect.mindcloud.co/v1/universal/grafana/latest/actions/export-mute-timings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grafana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grafana/latest/actions/export-mute-timings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grafana/latest/actions/export-mute-timings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "apiVersion": 1,
      "muteTimings": [
        {
          "name": "Ava Chen"
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
| `apiVersion` | number |  |
| `muteTimings[].name` | string |  |

## Native endpoint

Through the native Grafana API, this operation is `GET /v1/provisioning/mute-timings/export` (base URL `https://apps78aa.grafana.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-mute-timings.md) for the provider-specific parameters and requirements.

