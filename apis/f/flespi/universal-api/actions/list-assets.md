# Flespi: List assets



```
GET https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flespi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-assets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flespi/latest/actions/list-assets?${params}`, {
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
      "configuration": {},
      "id": 1,
      "name": "Ava Chen",
      "result": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configuration` | object | Asset configuration. |
| `id` | number | Asset ID. |
| `name` | string | Asset name. |
| `result` | array<object> | Flespi response result items. |

## Native endpoint

Through the native Flespi API, this operation is `GET /gw/assets/all` (base URL `https://flespi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assets.md) for the provider-specific parameters and requirements.

