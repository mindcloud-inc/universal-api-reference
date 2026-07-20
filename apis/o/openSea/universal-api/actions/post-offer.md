# OpenSea: Create Item Offer

Creates an item offer in OpenSea.

```
POST https://connect.mindcloud.co/v1/universal/openSea/latest/actions/post-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSea `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/post-offer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "chain": "string",
  "protocol": "string",
  "parameters": {},
  "protocolAddress": "string",
  "signature": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openSea/latest/actions/post-offer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "chain": "string",
    "protocol": "string",
    "parameters": {},
    "protocolAddress": "string",
    "signature": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `chain` | string | yes | The blockchain on which to filter the results |
| `protocol` | string | yes |  |
| `parameters` | object | yes |  |
| `protocolAddress` | string | yes |  |
| `signature` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |

## Native endpoint

Through the native OpenSea API, this operation is `POST /api/v2/orders/{chain}/{protocol}/offers` (base URL `https://api.opensea.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-offer.md) for the provider-specific parameters and requirements.

