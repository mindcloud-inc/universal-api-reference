# Fiserv: Capture Payment Intent

Captures a payment intent in Fiserv.

```
PUT https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/capture-payment-intent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiserv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/capture-payment-intent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "xAccountId": "string",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/capture-payment-intent', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "xAccountId": "string",
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `xAccountId` | string | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | string | yes | Payment intent id from the path. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fiserv API returns.

## Native endpoint

Through the native Fiserv API, this operation is `POST /payment_intents/{id}/capture` (base URL `https://bankinghub-cert.fiservapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/capture-payment-intent.md) for the provider-specific parameters and requirements.

