# ShipWise: Add Marketplace Inbound Mapping V2

Creates a marketplace inbound mapping in ShipWise.

```
POST https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/add-marketplace-inbound-mapping-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShipWise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/add-marketplace-inbound-mapping-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shipWise/latest/actions/add-marketplace-inbound-mapping-v2', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ShipWise API returns.

## Native endpoint

Through the native ShipWise API, this operation is `POST /api/v2/Marketplace/InboundMappings/Add` (base URL `https://api.shipwise.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-marketplace-inbound-mapping-v2.md) for the provider-specific parameters and requirements.

