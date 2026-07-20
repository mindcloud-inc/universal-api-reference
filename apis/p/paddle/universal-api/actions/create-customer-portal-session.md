# Paddle: Create Customer Portal Session

Creates a customer portal session in Paddle.

```
POST https://connect.mindcloud.co/v1/universal/paddle/latest/actions/create-customer-portal-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paddle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paddle/latest/actions/create-customer-portal-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paddle/latest/actions/create-customer-portal-session', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Paddle API returns.

## Native endpoint

Through the native Paddle API, this operation is `POST customers/{customer_id}/portal-sessions` (base URL `https://api.paddle.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer-portal-session.md) for the provider-specific parameters and requirements.

