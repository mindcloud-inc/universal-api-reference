# Fiserv: Update Checkout Session

Updates an existing checkout session in Fiserv.

```
PUT https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/update-checkout-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiserv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/update-checkout-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "xAccountId": "string",
  "id": "string",
  "requestBody": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/update-checkout-session', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "xAccountId": "string",
    "id": "string",
    "requestBody": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `xAccountId` | string | yes | Fiserv account id sent in the required x-account-id header. |
| `id` | string | yes | Checkout session id from the path. |
| `requestBody` | object | yes | JSON request body from the official update checkout session schema. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fiserv API returns.

## Native endpoint

Through the native Fiserv API, this operation is `PATCH /checkout_sessions/{id}` (base URL `https://bankinghub-cert.fiservapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-checkout-session.md) for the provider-specific parameters and requirements.

