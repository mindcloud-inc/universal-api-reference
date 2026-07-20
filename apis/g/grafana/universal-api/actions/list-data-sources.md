# Grafana: List Data Sources

Finds data sources in Grafana.

```
GET https://connect.mindcloud.co/v1/universal/grafana/latest/actions/list-data-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grafana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grafana/latest/actions/list-data-sources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grafana/latest/actions/list-data-sources?${params}`, {
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
      "id": 1,
      "isDefault": true,
      "name": "Ava Chen",
      "readOnly": true,
      "type": "string",
      "uid": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `isDefault` | boolean |  |
| `name` | string |  |
| `readOnly` | boolean |  |
| `type` | string |  |
| `uid` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Grafana API, this operation is `GET /datasources` (base URL `https://apps78aa.grafana.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-data-sources.md) for the provider-specific parameters and requirements.

