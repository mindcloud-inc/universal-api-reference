# Cryptolens: Set String Value

Updates a data object string value in Cryptolens.

```
PUT https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/set-string-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptolens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/set-string-value" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/set-string-value', {
  method: 'PUT',
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Set String Value acknowledgement message from the Cryptolens result envelope. |

## Native endpoint

Through the native Cryptolens API, this operation is `GET /api/data/SetStringValue` (base URL `https://api.cryptolens.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-string-value.md) for the provider-specific parameters and requirements.

