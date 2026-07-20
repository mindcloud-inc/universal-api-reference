# MRPeasy: Update Manufacturing Order

Updates an existing manufacturing order in MRPeasy.

```
PUT https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/update-manufacturing-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MRPeasy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/update-manufacturing-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "manOrdId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/update-manufacturing-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "manOrdId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `manOrdId` | number | yes | MRPeasy manufacturing order ID. |
| `quantity` | number | no | Updated manufacturing quantity. |
| `assignedId` | number | no | Updated MRPeasy assigned user ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MRPeasy API returns.

## Native endpoint

Through the native MRPeasy API, this operation is `PUT /manufacturing-orders/{{manOrdId}}` (base URL `https://api.mrpeasy.com/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-manufacturing-order.md) for the provider-specific parameters and requirements.

