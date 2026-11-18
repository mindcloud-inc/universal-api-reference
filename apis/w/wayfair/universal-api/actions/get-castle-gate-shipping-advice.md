# Wayfair: Get CastleGate Orders Shipping Advice



```
POST https://connect.mindcloud.co/v1/universal/wayfair/latest/actions/get-castle-gate-shipping-advice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wayfair `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wayfair/latest/actions/get-castle-gate-shipping-advice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wayfair/latest/actions/get-castle-gate-shipping-advice', {
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
| `limit` | number | no |  |
| `wsaIds` | string | no |  |
| `hasResponse` | string | no |  |
| `fromDate` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Wayfair API returns.

## Native endpoint

Through the native Wayfair API, this operation is `POST graphql` (base URL `https://{{credentials.environment}}.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-castle-gate-shipping-advice.md) for the provider-specific parameters and requirements.

