# OpenSea: Create Criteria Offer

Creates a criteria offer in OpenSea.

```
POST https://connect.mindcloud.co/v1/universal/openSea/latest/actions/post-criteria-offer-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OpenSea `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/openSea/latest/actions/post-criteria-offer-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "protocolData": {},
  "criteria": {},
  "protocolAddress": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/openSea/latest/actions/post-criteria-offer-v2', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "protocolData": {},
    "criteria": {},
    "protocolAddress": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `protocolData` | object | yes |  |
| `criteria` | object | yes |  |
| `protocolAddress` | string | yes |  |

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

Through the native OpenSea API, this operation is `POST /api/v2/offers` (base URL `https://api.opensea.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-criteria-offer-v2.md) for the provider-specific parameters and requirements.

