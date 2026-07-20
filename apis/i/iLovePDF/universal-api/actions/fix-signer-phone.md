# iLovePDF: Fix Signer Phone

Updates a signer phone number in an iLovePDF signature request.

```
PUT https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/fix-signer-phone
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a iLovePDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/fix-signer-phone" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/iLovePDF/latest/actions/fix-signer-phone', {
  method: 'PUT',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "access_code": true,
      "email": "ava@example.com",
      "force_signature_type": "string",
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "status": "string",
      "token_requester": "string",
      "type": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `access_code` | boolean |  |
| `email` | string |  |
| `force_signature_type` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `status` | string |  |
| `token_requester` | string |  |
| `type` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native iLovePDF API, this operation is `PUT https://:server/v1/signature/signer/fix-phone/:signerTokenRequester` (base URL `https://api.ilovepdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fix-signer-phone.md) for the provider-specific parameters and requirements.

