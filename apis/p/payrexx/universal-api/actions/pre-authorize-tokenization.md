# Payrexx: Pre-Authorize Tokenization

Pre-authorizes a tokenization in Payrexx.

```
POST https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/pre-authorize-tokenization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payrexx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/pre-authorize-tokenization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "123456"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payrexx/latest/actions/pre-authorize-tokenization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "123456"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the transaction to pre-authorize. Example: `123456`. |
| `amount` | number | no | Amount for pre-authorization in cents. Example: `1000`. |
| `purpose` | string | no | The purpose of the pre-authorization. Example: `MindCloud pre-authorization test`. |
| `referenceId` | string | no | Reference ID for the pre-authorized transaction. Example: `mc-preauth-001`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Payrexx API returns.

## Native endpoint

Through the native Payrexx API, this operation is `POST Transaction/:id/preAuthorize` (base URL `https://api.payrexx.com/v1.14/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pre-authorize-tokenization.md) for the provider-specific parameters and requirements.

