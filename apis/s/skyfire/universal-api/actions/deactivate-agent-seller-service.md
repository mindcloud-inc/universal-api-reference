# Skyfire: Deactivate Agent Seller Service

Deactivates an existing agent seller service in Skyfire.

```
PUT https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/deactivate-agent-seller-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/deactivate-agent-seller-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sellerServiceId": "seller-service-id"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/deactivate-agent-seller-service', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sellerServiceId": "seller-service-id"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sellerServiceId` | string | yes | The ID of the seller service to deactivate. Example: `seller-service-id`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Skyfire API returns.

## Native endpoint

Through the native Skyfire API, this operation is `POST /agents/seller-services/:sellerServiceId/deactivate` (base URL `https://api.skyfire.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/deactivate-agent-seller-service.md) for the provider-specific parameters and requirements.

