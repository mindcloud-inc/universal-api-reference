# Dash.app: Search Asset Download Events

Finds asset download events in Dash.app by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/search-asset-download-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dash.app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/search-asset-download-events?connectionId=$CONNECTION_ID&criterion=%5Bobject%20Object%5D&from=0&pageSize=100&sorts%5B%5D=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "criterion": "[object Object]",
  "from": "0",
  "pageSize": "100",
  "sorts[]": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/search-asset-download-events?${params}`, {
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
| `criterion` | object | yes | Example: `[object Object]`. |
| `from` | number | yes | Default: `0`. |
| `pageSize` | number | yes | Default: `100`. |
| `sorts[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aggregations": {},
      "results": [
        {}
      ],
      "totalResults": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aggregations` | object |  |
| `results` | array<object> |  |
| `totalResults` | number |  |

## Native endpoint

Through the native Dash.app API, this operation is `POST /asset-download-event-searches` (base URL `https://api-v2.dash.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-asset-download-events.md) for the provider-specific parameters and requirements.

