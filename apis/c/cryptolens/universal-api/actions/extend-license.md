# Cryptolens: Extend License

Extends a license in Cryptolens.

```
PUT https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/extend-license
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptolens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/extend-license" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": 1,
  "key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/extend-license', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": 1,
    "key": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | number | yes | The product id. |
| `key` | string | yes | The serial key string. |

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
| `message` | string | Extend License acknowledgement message from the Cryptolens result envelope. |

## Native endpoint

Through the native Cryptolens API, this operation is `GET /api/key/ExtendLicense` (base URL `https://api.cryptolens.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extend-license.md) for the provider-specific parameters and requirements.

