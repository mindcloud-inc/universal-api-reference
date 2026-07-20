# Skribble: Update Signature Request Signers

Updates the signer list for a signature request in Skribble.

```
PUT https://connect.mindcloud.co/v1/universal/skribble/latest/actions/update-signature-request-signers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/skribble/latest/actions/update-signature-request-signers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureRequestId": "string",
  "signatures[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skribble/latest/actions/update-signature-request-signers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signatureRequestId": "string",
    "signatures[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signatureRequestId` | string | yes | The signature request ID to update. |
| `signatures[]` | array<object> | yes | The complete signer list to keep on the signature request. |
| `title` | string | no | Optional replacement title. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Skribble API returns.

## Native endpoint

Through the native Skribble API, this operation is `PUT /v2/signature-requests` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-signature-request-signers.md) for the provider-specific parameters and requirements.

