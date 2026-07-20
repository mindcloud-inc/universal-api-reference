# Socket: Get Alert Types Metadata

Retrieves alert type metadata from Socket.

```
POST https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-alert-types-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-alert-types-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-alert-types-metadata', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[]` | array<object> |  |
| `items[].description` | string |  |
| `items[].emoji` | string |  |
| `items[].nextStepTitle` | string |  |
| `items[].props` | object |  |
| `items[].suggestion` | string |  |
| `items[].title` | string |  |
| `items[].type` | string |  |

## Native endpoint

Through the native Socket API, this operation is `POST /alert-types` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-alert-types-metadata.md) for the provider-specific parameters and requirements.

