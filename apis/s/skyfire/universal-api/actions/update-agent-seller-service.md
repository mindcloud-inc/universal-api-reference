# Skyfire: Update Agent Seller Service

Updates an existing agent seller service in Skyfire.

```
PUT https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/update-agent-seller-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skyfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/update-agent-seller-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sellerServiceId": "seller-service-id"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skyfire/latest/actions/update-agent-seller-service', {
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
| `description` | string | no | New description of the service. |
| `name` | string | no | New name of the service. |
| `sellerServiceId` | string | yes | The ID of the seller service to update. Example: `seller-service-id`. |
| `tags[]` | array<string> | no | New tags for the service. Example: `api,agent-tools`. |
| `minimumTokenAmount` | string | no | New minimum amount in USD that buyers must set on their tokens. Example: `0.01`. |
| `price` | string | no | New price of the service in USD. Example: `0.01`. |
| `acceptedTokens[]` | array<string> | no | List of token types the seller service accepts. Must be one or more of kya, pay, and kya-pay. Example: `pay,kya-pay`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Skyfire API returns.

## Native endpoint

Through the native Skyfire API, this operation is `PATCH /agents/seller-services/:sellerServiceId` (base URL `https://api.skyfire.xyz/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-agent-seller-service.md) for the provider-specific parameters and requirements.

