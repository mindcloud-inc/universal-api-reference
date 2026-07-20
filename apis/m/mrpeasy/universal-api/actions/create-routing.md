# MRPeasy: Create Routing

Creates a new routing in MRPeasy.

```
POST https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/create-routing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MRPeasy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/create-routing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": 1,
  "title": "string",
  "operations": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/create-routing', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": 1,
    "title": "string",
    "operations": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `productId` | number | yes | MRPeasy product ID for the routing. |
| `title` | string | yes | Routing title. |
| `operations` | array<object> | yes | Array of routing operations, for example [{"type_id":1,"ord":"1","description":"Op","fixed_time":1,"variable_time":1,"variable_quantity":1,"time_payment":true}]. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MRPeasy API returns.

## Native endpoint

Through the native MRPeasy API, this operation is `POST /routings` (base URL `https://api.mrpeasy.com/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-routing.md) for the provider-specific parameters and requirements.

