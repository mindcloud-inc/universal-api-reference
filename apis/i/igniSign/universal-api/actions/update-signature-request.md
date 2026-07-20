# IgniSign: Update Signature Request



```
PUT https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/update-signature-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IgniSign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/update-signature-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "signatureRequestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/igniSign/latest/actions/update-signature-request', {
  method: 'PUT',
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
| `signatureRequestId` | string | yes | The IgniSign signature request ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "documentIds": [
        "string"
      ],
      "documents": [
        {}
      ],
      "signerIds": [
        "string"
      ],
      "signers": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `documentIds` | array<string> |  |
| `documents` | array<object> |  |
| `signerIds` | array<string> |  |
| `signers` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native IgniSign API, this operation is `PUT /v4/signature-requests/:signatureRequestId` (base URL `https://api.ignisign.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-signature-request.md) for the provider-specific parameters and requirements.

