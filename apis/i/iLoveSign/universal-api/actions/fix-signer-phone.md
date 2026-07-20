# iLoveSign: Fix Signer Phone



```
PUT https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/fix-signer-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLoveSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/fix-signer-phone" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signerTokenRequester": "string",
  "phone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iLoveSign/latest/actions/fix-signer-phone', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signerTokenRequester": "string",
    "phone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signerTokenRequester` | string | yes | Signer token requester identifier. |
| `phone` | string | yes | Replacement mobile number including country prefix digits only. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native iLoveSign API returns.

## Native endpoint

Through the native iLoveSign API, this operation is `PUT /signature/signer/fix-phone/:signer_token_requester` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fix-signer-phone.md) for the provider-specific parameters and requirements.

