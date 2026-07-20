# Absinthe: Refund a Redemption

Refunds a redemption for a user in Absinthe.

```
POST https://connect.mindcloud.co/v1/universal/absinthe/latest/actions/refund-a-redemption
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Absinthe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/absinthe/latest/actions/refund-a-redemption" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "refundReason": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/absinthe/latest/actions/refund-a-redemption', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "refundReason": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `redemptionId` | string | no |  |
| `refundReason` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Absinthe API returns.

## Native endpoint

Through the native Absinthe API, this operation is `POST /redemptions/{redemption_id}/refund` (base URL `https://api.absinthe.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refund-a-redemption.md) for the provider-specific parameters and requirements.

