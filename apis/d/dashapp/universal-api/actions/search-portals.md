# Dash.app: Search Portals

Finds portals in Dash.app by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/search-portals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dash.app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/search-portals?connectionId=$CONNECTION_ID&criterion=%5Bobject%20Object%5D&from=0&pageSize=100&sorts%5B%5D=%5Bobject%20Object%5D" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/search-portals?${params}`, {
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
| `criterion` | object | yes | Portal search criterion object. Example: `[object Object]`. |
| `from` | number | yes | Zero-based result offset. Default: `0`. |
| `pageSize` | number | yes | Maximum number of results to return. Default: `100`. |
| `sorts[]` | array<object> | yes | Array of portal sort objects. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `results` | array<object> |  |
| `totalResults` | number |  |

## Native endpoint

Through the native Dash.app API, this operation is `POST /portal-searches` (base URL `https://api-v2.dash.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-portals.md) for the provider-specific parameters and requirements.

