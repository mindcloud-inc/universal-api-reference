# Mux: Create an Asset



```
POST https://connect.mindcloud.co/v1/universal/mux/latest/actions/create-an-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mux/latest/actions/create-an-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputs[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mux/latest/actions/create-an-asset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputs[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputs[]` | array<object> | yes | The input sources for the asset. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |

## Native endpoint

Through the native Mux API, this operation is `POST /video/v1/assets` (base URL `https://api.mux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-an-asset.md) for the provider-specific parameters and requirements.

