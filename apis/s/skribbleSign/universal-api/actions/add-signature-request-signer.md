# Skribble Sign: Add Signature Request Signer

Adds a signer to a signature request in Skribble Sign.

```
POST https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/add-signature-request-signer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Skribble Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/add-signature-request-signer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureRequestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/skribbleSign/latest/actions/add-signature-request-signer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "signatureRequestId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signatureRequestId` | string | yes | The signature request ID. |
| `accountEmail` | string | no | The signer account email. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `signerIdentityData` | object | no | Optional signer identity payload for no-account signers. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_email": "ava@example.com",
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_email` | string | Signer account email. |
| `id` | string | Signature ID. |
| `status` | string | Signer status. |

## Native endpoint

Through the native Skribble Sign API, this operation is `POST /v2/signature-requests/:signatureRequestId/signatures` (base URL `https://api.skribble.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-signature-request-signer.md) for the provider-specific parameters and requirements.

