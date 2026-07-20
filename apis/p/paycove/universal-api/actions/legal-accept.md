# Paycove: Legal Accept

Creates a legal acceptance token in Paycove.

```
POST https://connect.mindcloud.co/v1/universal/paycove/latest/actions/legal-accept
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paycove `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/legal-accept" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accepterEmail": "ava@example.com",
  "returnUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paycove/latest/actions/legal-accept', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accepterEmail": "ava@example.com",
    "returnUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accepterEmail` | string | yes | The email address accepting the legal terms. |
| `returnUrl` | string | yes | Where the signer returns after accepting the legal terms. |
| `state` | string | no | Optional opaque state value to round-trip through the acceptance flow. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Paycove API returns.

## Native endpoint

Through the native Paycove API, this operation is `POST accounts/legal-accept` (base URL `https://paycove.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/legal-accept.md) for the provider-specific parameters and requirements.

