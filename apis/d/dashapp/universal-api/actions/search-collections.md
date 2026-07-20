# Dash.app: Search Collections

Finds collections in Dash.app by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/search-collections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dash.app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/search-collections?connectionId=$CONNECTION_ID&from=0&pageSize=100&criterion=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "0",
  "pageSize": "100",
  "criterion": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/search-collections?${params}`, {
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
| `from` | number | yes | The item number to begin the result set from. Default: `0`. |
| `pageSize` | number | yes | The maximum number of items to return. Default: `100`. |
| `criterion` | object | yes | Dash collection search criterion object. Example: `[object Object]`. |
| `sorts[]` | array<object> | no | Dash collection sort array. Example: `[object Object]`. |

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

Through the native Dash.app API, this operation is `POST /collection-searches` (base URL `https://api-v2.dash.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-collections.md) for the provider-specific parameters and requirements.

